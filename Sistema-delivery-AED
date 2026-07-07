
def calcular_costo_envio(zona):
    zona = zona.capitalize()
    if zona == "Centro":
        return 500, "Centro"
    elif zona == "Norte":
        return 800, "Norte"
    elif zona == "Sur":
        return 900, "Sur"
    else:
        return 1200, "Periferia / Otra"

def validar_numero(mensaje):
    while True:
        try:
            return float(input(mensaje))
        except ValueError:
            print("Error: Por favor, ingrese un valor numérico válido.")

def registrar_pedido():
    print("\n=== REGISTRO DE NUEVO PEDIDO ===")
    cliente = input("Ingrese el nombre del cliente: ")
    producto = input("Ingrese el producto solicitado: ")
    precio_producto = validar_numero("Ingrese el precio del producto: $")
    zona_ingresada = input("Ingrese la zona (Centro / Norte / Sur): ")
    
    costo_envio, zona_final = calcular_costo_envio(zona_ingresada)
    importe_total = precio_producto + costo_envio
    
    print("\nEstados: 1-En preparación, 2-En camino, 3-Entregado")
    codigo_estado = int(validar_numero("Ingrese número de estado (1-3): "))
    
    if codigo_estado == 1:
        estado_texto = "En preparación 🍳"
    elif codigo_estado == 2:
        estado_texto = "En camino / Repartidor asignado 🏍️"
    elif codigo_estado == 3:
        estado_texto = "Entregado con éxito ✅"
    else:
        estado_texto = "Estado desconocido"

    # --- TICKET ---
    print("\n" + "="*40)
    print("           TICKET DE DELIVERY           ")
    print("="*40)
    print(f"Cliente: {cliente}")
    print(f"Producto: {producto}")
    print(f"Precio base: ${precio_producto:.2f}")
    print(f"Zona: {zona_final} | Envío: ${costo_envio}")
    print("-" * 40)
    print(f"TOTAL A ABONAR: ${importe_total:.2f}")
    print(f"Estado: {estado_texto}")
    print("="*40)
    input("\nPresione Enter para volver al menú...")

def main():
    while True:
        print("\n--- SISTEMA DE DELIVERY ---")
        print("1. Registrar nuevo pedido")
        print("2. Salir")
        opcion = input("Seleccione una opción: ")

        if opcion == "1":
            registrar_pedido()
        elif opcion == "2":
            print("Saliendo del sistema. ¡Hasta luego!")
            break
        else:
            print("Opción inválida, intente nuevamente.")

if __name__ == "__main__":
    main()
