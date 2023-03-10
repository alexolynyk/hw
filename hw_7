import random
print("Let's play!")
file = open('homework_7.txt', 'r')
n = file.read()
best_score = int(n.split()[2])

while True:
    my_number = random.choice(range(101))
    counting = 1

    def func(your_number):
        if your_number > my_number:
            print('Try a smaller number')
        elif your_number < my_number:
            print('Try a higher number')


    while True:
        your_number = input('Write number from 0 to 100: ')
        if not your_number.isdigit():
            print('It is not a number')
        elif int(your_number) == my_number:
            print(f'You WON and made {counting} tries')
            if counting <= best_score:
                best_score = counting
                print('It is the best score')
                hw_file = open('homework_7.txt', 'w')
                print('Best score: ', best_score, file=hw_file)
                hw_file.close()
            else:
                print(f'Good, but not perfect. \nThe best score is {best_score}')
            break
        else:
            counting += 1
            your_number = int(your_number)
            func(your_number)

    answer = input('Do you wanna play more? Write "Yes": ')
    if not answer.upper() == 'YES':
        break
