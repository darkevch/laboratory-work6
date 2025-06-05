import random

institutions = {}

def generate_random_data(num_institutions):
    types = ["Школа", "Коледж"]
    for i in range(num_institutions):
        institution_type = random.choice(types)
        name = f"{institution_type}_{i+1}"
        students_count = random.randint(50, 200)  # Кількість учнів (50-200)
        gym_visits = random.randint(10, 50)  # Відвідування спортзалу (10-50)
        institutions[name] = (students_count, gym_visits)

def display_dictionary():
    if not institutions:
        print("Словник порожній.")
    else:
        print("\nЗміст словника:")
        for name, data in institutions.items():
            print(f"Заклад: {name}, Кількість учнів: {data[0]}, Відвідувань спортзалу: {data[1]}")

def total_students():
    total = sum(data[0] for data in institutions.values())
    print(f"\nЗагальна кількість учнів по всіх закладах: {total}")

def add_institution():
    name = input("Введіть назву закладу (наприклад, Школа_1 або Коледж_1): ")
    if name in institutions:
        print("Заклад з такою назвою уже існує!")
        return
    try:
        students_count = int(input("Введіть кількість учнів: "))
        gym_visits = int(input("Введіть кількість відвідувань спортзалу: "))
        institutions[name] = (students_count, gym_visits)
        print(f"Заклад {name} успішно доданий.")
    except ValueError:
        print("Помилка: введіть числові значення для кількості учнів та відвідувань.")

def remove_institution():
    name = input("Введіть назву закладу для видалення: ")
    if name in institutions:
        del institutions[name]
        print(f"Заклад {name} успішно видалений.")
    else:
        print("Закладу з такою назвою не знайдено.")

def display_sorted():
    if not institutions:
        print("Словник порожній.")
    else:
        sorted_keys = sorted(institutions.keys())
        print("\nЗміст словника (відсортований за ключами):")
        for name in sorted_keys:
            data = institutions[name]
            print(f"Заклад: {name}, Кількість учнів: {data[0]}, Відвідувань спортзалу: {data[1]}")

def main():
    print("Програма для управління словником навчальних закладів (варіант 3, n=6).")
    generate_random_data(6)
    display_dictionary()
    total_students()

    while True:
        print("\nМеню:")
        print("1. Показати словник")
        print("2. Підрахувати загальну кількість учнів")
        print("3. Додати заклад")
        print("4. Видалити заклад")
        print("5. Показати словник, відсортований за ключами")
        print("6. Вийти")
        
        choice = input("Виберіть опцію (1-6): ")
        
        if choice == "1":
            display_dictionary()
        elif choice == "2":
            total_students()
        elif choice == "3":
            add_institution()
        elif choice == "4":
            remove_institution()
        elif choice == "5":
            display_sorted()
        elif choice == "6":
            print("Програма завершена.")
            break
        else:
            print("Невірний вибір. Спробуйте ще раз.")

if __name__ == "__main__":
    main()
