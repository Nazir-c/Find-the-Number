import random

def guess_the_number():
    number_to_guess = random.randint(1, 100)
    guess = None
    attempts = 0

    print("Добро пожаловать в игру 'Угадай число'!")
    print("Я загадал число от 1 до 100.")
    print("Попробуйте угадать его!")

    while guess != number_to_guess:
        try:
            guess = int(input("Введите ваше предположение: "))
            attempts += 1

            if guess < number_to_guess:
                print("Слишком мало! Попробуйте снова.")
            elif guess > number_to_guess:
                print("Слишком много! Попробуйте снова.")
            else:
                print(f"Поздравляем! Вы угадали число с {attempts} попыток.")
        except ValueError:
            print("Некорректный ввод. Пожалуйста, введите число.")

if __name__ == "__main__":
    guess_the_number()  
