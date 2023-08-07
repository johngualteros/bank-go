## Models.go

es importante recalcar que en go no existen las 
clases como en otros lenguajes de programacion
por ende en go se usan type stuct que es
muy similar donde se especifica el nombre y tipo

## Db.go

type se utiliza para definir y declarar una interfaz se usa para 
darle el nombre con el cual se puede referenciar

Los punteros son útiles en varias situaciones, como:

Pasar valores grandes o complejos a funciones de manera más eficiente, ya que solo se pasa la dirección en lugar de duplicar todo el valor.
Permitir que una función modifique el valor original de una variable al trabajar con su puntero.
Evitar la copia de datos en situaciones donde se necesitan cambios en un valor compartido (como en las estructuras compartidas entre varios componentes).
Trabajar con estructuras de datos en tiempo real, como colas y listas enlazadas.

cuando una variable tiene &nombreVariable es porque accede al 
valor en memoria de dicha variable

:= declara y instancia normalmente se usa 
en un scope local
nil es nulo
_ es un identificador en blanco


defer es útil para asegurarse de que ciertas acciones se realicen, independientemente de cómo o cuándo una función termine, lo que puede ayudar a evitar fugas de recursos o a garantizar la consistencia en la manipulación de datos.

como hacer el num, err
func divide(a, b float64) (float64, error) {
if b == 0 {
return 0, fmt.Errorf("división por cero")
}
return a / b, nil
}

func main() {
result, err := divide(10, 2)
if err != nil {
fmt.Println("Error:", err)
} else {
fmt.Println("Resultado:", result)
}
}
