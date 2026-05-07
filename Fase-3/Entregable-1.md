                                                  **CheckPoint**
                                                  
                                                  
---

#¿Puedo explicar a un compañero cuándo elegir lista doble vs. simple vs. arreglo, con ejemplos concretos?

   -Un arreglo tiene un superpoder que es el acceso instantaneo por indice.
       por ejemplo: Si vas a un numero de piso exacto en un edificio y sabes cual es, vas directo a el sin tener que revisar cada uno.
        (Puedes elegir este metodo cuando sabes exactamente tendras)

    -Lista enlazada simple ahorra memoria y tiene fluidez al insertar.
       por ejemplo: Cada pista te guia a la siguiente.
        (Puedes elegirlo cuando tienes memoria limitada y necesitas procesar los datos de principio a fin)

   -La lista doblemente enlazada es bidirecional.
      por ejemplo: Un tren, puedes caminar del vagon 1 hasta el 5 y regresar desde el 5 al 1 sin probelmas
        (Puedes usarlo cuando necesitas navegar en ambas direcciones como con las playlist )


---


  #¿Qué patrón descubrí al implementar? ¿Hay una "receta" para las operaciones de lista doble?

      -No importa si estas insertando al inicio o al final, siempre sigues la secuencia logica para no perder los nodos.
      Esto quiere decire que primero se unen los nuevos puentes antes de eliminar los demas, si rompes un enlace antes de asegurar el nuevo, tu lsta se "suelta" por asi decirlo
        Se podria decir que "la receta" es: configurar el nuevo nodo y enlazarlo

---

#Si tuviera que enseñar "listas dobles" a alguien, ¿por dónde empezaría y qué diagrama dibujaría primero?

      -Empezaria por explicarle sobre que son los nodos y no son mas que un punto de conexion, teniendo eso en mente, le explicaria la analogia del tren, creo que es la mas sencilla


        
  




      
