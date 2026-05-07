
Error insertar final: 

    void insertarFinal(string valor) {
    NodoDoble* nuevo = new NodoDoble(valor);

    if (cola == nullptr) {
        cabeza = cola = nuevo;
    } else {
        nuevo->ant = cola;
        cola->sig = nuevo;

        cola = nuevo;

        // BUG: línea innecesaria 
        cola->sig = nullptr;
     }
    }


El constructor ya inicializa sig = nullptr, esto no rompe el programa directamente, pero puede ocultar errores de conexion previa.

    Version corregida:

    void insertarFinal(string valor) {
    NodoDoble* nuevo = new NodoDoble(valor);

    if (cola == nullptr) {
        cabeza = cola = nuevo;
    } else {
        nuevo->ant = cola;
        cola->sig = nuevo;
        cola = nuevo;
    }
     }
 


---


Eliminar Nodo:

    void eliminarNodo(NodoDoble* nodo) {
    if (nodo == nullptr) return;

    nodo->ant->sig = nodo->sig;
    nodo->sig->ant = nodo->ant;

    if (nodo == cabeza) {
        cabeza = nodo->sig;
    }

    if (nodo == cola) {
        cola = nodo->ant;
    }

    delete nodo;
    }

 Esta lista tiene un solo nodo y se crashes inmediatamente y el programa se detiene.

   Version corregida:

   void eliminarNodo(NodoDoble* nodo) {
    if (nodo == nullptr) return;

    // caso único
    if (nodo == cabeza && nodo == cola) {
        cabeza = cola = nullptr;
        delete nodo;
        return;
    }

    if (nodo->ant != nullptr)
        nodo->ant->sig = nodo->sig;
    else
        cabeza = nodo->sig;

    if (nodo->sig != nullptr)
        nodo->sig->ant = nodo->ant;
    else
        cola = nodo->ant;

    delete nodo;
    }


---


Romper simetria:

    void conectarNodos(NodoDoble* a, NodoDoble* b) {
    a->sig = b;

    // BUG: rompe bidireccionalidad
    b->ant = a->ant;
    }

Si A apunta a B entonces deberia ser B->ant=A, pero dice “B cree que su anterior es el anterior de A” y rompe la cadena

Version corregida:

    void conectarNodos(NodoDoble* a, NodoDoble* b) {
    a->sig = b;
    b->ant = a;
    }





