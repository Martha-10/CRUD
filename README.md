inventario = {
    '001': {'nombre': 'Manzanas', 'cantidad': 50, 'precio': 0.5},
    '002': {'nombre': 'Bananas', 'cantidad': 30, 'precio': 0.3},
    # ... otros productos
}
def agregar_producto():
    codigo = input("Ingrese el código del producto: ")
    if codigo in inventario:
        print("El producto ya existe.")
        return
    nombre = input("Ingrese el nombre del producto: ")
    cantidad = int(input("Ingrese la cantidad: "))
    precio = float(input("Ingrese el precio: "))
    inventario[codigo] = {'nombre': nombre, 'cantidad': cantidad, 'precio': precio}
    print("Producto agregado exitosamente.")
    
def mostrar_inventario():
    if not inventario:
        print("El inventario está vacío.")
        return
    print("\nInventario:")
    print("{:<10} {:<15} {:<10} {:<10}".format('Código', 'Nombre', 'Cantidad', 'Precio'))
    for codigo, datos in inventario.items():
        print("{:<10} {:<15} {:<10} {:<10.2f}".format(codigo, datos['nombre'], datos['cantidad'], datos['precio']))

        def actualizar_producto():
    codigo = input("Ingrese el código del producto a actualizar: ")
    if codigo not in inventario:
        print("El producto no existe.")
        return
    nombre = input("Ingrese el nuevo nombre del producto: ")
    cantidad = int(input("Ingrese la nueva cantidad: "))
    precio = float(input("Ingrese el nuevo precio: "))
    inventario[codigo] = {'nombre': nombre, 'cantidad': cantidad, 'precio': precio}
    print("Producto actualizado exitosamente.")

    def eliminar_producto():
    codigo = input("Ingrese el código del producto a eliminar: ")
    if codigo in inventario:
        del inventario[codigo]
        print("Producto eliminado exitosamente.")
    else:
        print("El producto no existe.")
def menu():
    while True:
        print("\n--- Sistema de Inventario ---")
        print("1. Agregar producto")
        print("2. Mostrar inventario")
        print("3. Actualizar producto")
        print("4. Eliminar producto")
        print("5. Salir")
        opcion = input("Seleccione una opción: ")

        if opcion == '1':
            agregar_producto()
        elif opcion == '2':
            mostrar_inventario()
        elif opcion == '3':
            actualizar_producto()
        elif opcion == '4':
            eliminar_producto()
        elif opcion == '5':
            print("Saliendo del sistema.")
            break
        else:
            print("Opción no válida. Intente nuevamente.")
if __name__ == "__main__":
    menu()


