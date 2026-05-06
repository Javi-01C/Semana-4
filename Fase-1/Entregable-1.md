

                    --Insertar 3 al inicio--
            Lista inicial:        

null <-- [7] <--> [15] <--> [23] <--> [42] --> null     "Agregar el nuevo nodo [3]"
         ^                                   ^
      cabeza                               cola
      
      Despues...
 null <-- [3] <--> [7] <--> [15] <--> [23] <--> [42] --> null
         ^                                       ^
      cabeza (cambia de 7 a 3)                  cola(no cambia)


                     --Insertar 50 al final--

               Lista inicial:      
                     
 null <-- [3] <--> [7] <--> [15] <--> [23] <--> [42] --> null
         ^                                       ^
      cabeza                                   cola                    
      
    Despues...

null <-- [3] <--> [7] <--> [15] <--> [23] <--> [42] <--> [50] --> null
         ^                                               ^
      cabeza (no cambia)                               cola (cabia de 42 a 50)



            --Eliminar nodo con valor 15--

      Lista inicial:      
      
null <-- [3] <--> [7] <--> [15] <--> [23] <--> [42] <--> [50] --> null
         ^                                               ^
      cabeza                                           cola


      Despues...

null <-- [3] <--> [7] <--> [23] <--> [42] <--> [50] --> null
         ^                                           ^
      cabeza                                       cola

       (No cambian ni cabeza ni cola)

---

**Por qué eliminar un nodo conocido es O(1) en la lista doble pero O(n) en la lista simple**  

     -En una lista doblemente enlazada, cada nodo tiene referencia al siguiente y al anterior nodo, por lo tanto no se necesita recorrer la lista.

    -Por otra parte, en una lista simple cada nodo solo tiene referencia al siguiente nodo, no sabes quien esta detras, por lo tanto si necesitas recorrer la lista y esto puedo tomar hasta "n" pasos --> O(n).



