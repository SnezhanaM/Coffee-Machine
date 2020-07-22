class CoffeeMachine:
    def __init__(self):
        self.resources = [400, 540, 120, 9, 550]
        self.espresso = [250, 0, 16, 1, -4]
        self.latte = [350, 75, 20, 1, -7]
        self.cappuccino = [200, 100, 12, 1, -6]
        self.resources_name = ['water', 'milk', 'coffee', 'cups', 'money']

    def buy(self, drink):
        for i in range(4):
            if drink[i] > self.resources[i]:
                print(f'Sorry, not enough {self.resources_name[i]}!')
                break
        else:
            print('I have enough resources, making you a coffee!')
            for i in range(5):
                self.resources[i] -= drink[i]
        return self.resources

    def fill(self):
        print('\nWrite how many ml of water do you want to add:')
        self.resources[0] += int(input())
        print('Write how many ml of milk do you want to add:')
        self.resources[1] += int(input())
        print('Write how many grams of coffee beans do you want to add:')
        self.resources[2] += int(input())
        print('Write how many disposable cups of coffee do you want to add:')
        self.resources[3] += int(input())
        return self.resources

    def menu(self):
        while True:
            print("Write action (buy, fill, take, remaining, exit):")
            user_action = input()
            if user_action == 'buy':
                print("\nWhat do you want to buy? 1 - espresso, 2 - latte, 3 - cappuccino:")
                user_input = input()
                if user_input == '1':
                    self.buy(self.espresso)
                elif user_input == '2':
                    self.buy(self.latte)
                elif user_input == '3':
                    self.buy(self.cappuccino)
                elif user_input == 'back':
                    continue
                print()
            elif user_action == 'fill':
                self.resources = self.fill()
                print()
            elif user_action == 'take':
                print(f'I gave you {self.resources[4]}')
                self.resources[4] = 0
                print()
            elif user_action == 'remaining':
                print(f"""\nThe coffee machine has:
{self.resources[0]} of water
{self.resources[1]} of milk
{self.resources[2]} of coffee beans
{self.resources[3]} of disposable cups
${self.resources[4]} of money\n""")
            elif user_action == 'exit':
                break

if __name__ == '__main__':
    CoffeeMachine().menu()
