# calculadora-pro-python
Calculadora en Python con múltiples operaciones y validación de errores
while True:
    print("\n=== CALCULADORA PRO ===")

    # Validar números
    try:
        num1 = float(input("Ingresa el primer número: "))
        num2 = float(input("Ingresa el segundo número: "))
    except:
        print("❌ Error: ingresa solo números")
        continue

    # Menú
    print("\nOperaciones:")
    print("1. Sumar")
    print("2. Restar")
    print("3. Multiplicar")
    print("4. Dividir")
    print("5. Potencia (num1 ^ num2)")
    print("6. Módulo (residuo)")

    opcion = input("Elige una opción (1-6): ")

    print("\n--- Resultado ---")

    if opcion == "1":
        print("Resultado:", num1 + num2)

    elif opcion == "2":
        print("Resultado:", num1 - num2)

    elif opcion == "3":
        print("Resultado:", num1 * num2)

    elif opcion == "4":
        if num2 != 0:
            print("Resultado:", num1 / num2)
        else:
            print("❌ No se puede dividir por 0")

    elif opcion == "5":
        print("Resultado:", num1 ** num2)

    elif opcion == "6":
        if num2 != 0:
            print("Resultado:", num1 % num2)
        else:
            print("❌ No se puede hacer módulo con 0")

    else:
        print("❌ Opción inválida")

    # Repetir
    salir = input("\n¿Quieres seguir? (s/n): ")
    if salir.lower() != "s":
        print("👋 Gracias por usar la calculadora")
        break
