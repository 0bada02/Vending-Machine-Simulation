# Vending Machine Simulation

This is a Java 17-based vending machine simulation. The project allows users to interact as buyers or owners, providing functionalities for purchasing items, managing inventory, and handling payments.

## Features

- **Buyer Mode:**
  - View available items
  - Purchase items with automated change calculation
  - Receive a message if the machine lacks sufficient change

- **Owner Mode:**
  - Add new items
  - Remove items
  - Refill the vending machine
  - View available items
  - View available money

## Program Flow

### Start Program
```
Who are you?
1. Buyer.
2. Owner.
3. Exit.
```

### Owner Operations
```
What you want?
1. Add Item.
2. Remove Item.
3. Fill Machine.
4. Show Items.
5. Show Moneys.
6. Exit.
```

### Buyer Operations
```
What you want?
1. Show Items.
2. Buy Item.
3. Exit.
```

### Viewing Items
```
ID  | Name       | Price   | Quantity
--------------------------------------
1   | Candy      | 0.50    | 20     
2   | Chips      | 0.75    | 10     
```

### Viewing Money in Machine
```
Amount     | Count
-------------------
00.01 JD   | 0      
00.05 JD   | 0      
00.10 JD   | 0      
00.25 JD   | 50     
00.50 JD   | 20     
01.00 JD   | 5      
05.00 JD   | 0      
10.00 JD   | 0      
20.00 JD   | 0      
50.00 JD   | 0      
__________________
Total: 27.50 JD
```

### Buying an Item
#### Successful Purchase
```
ID  | Name       | Price   | Quantity
--------------------------------------
1   | Candy      | 0.50    | 20     
Enter the item ID you want to buy: 1
How many do you want: 3
This item is available.
Required amount 1.50 JD: 1
Amount paid 1.000 JD, Enter remaining amount 0.500 JD: 0.20
Amount paid 1.200 JD, Enter remaining amount 0.300 JD: 0.10
Amount paid 1.300 JD, Enter remaining amount 0.200 JD: 0.10
Amount paid 1.400 JD, Enter remaining amount 0.100 JD: 0.05
Amount paid 1.450 JD, Enter remaining amount 0.050 JD: 0.05
The rest of the amount 0.00 JD, Thank you for purchasing (:
```

#### Insufficient Change in Machine
```
ID  | Name       | Price   | Quantity
--------------------------------------
1   | Candy      | 0.50    | 17     
Enter the item ID you want to buy: 1
How many do you want: 5
This item is available.
Required amount 2.50 JD: 50
Sorry, there is no money in the machine.
```

#### Change Remaining After Purchase
```
The rest of the amount 0.50 JD, Thank you for purchasing (:
```

### Money in Machine After Change Dispensed
```
Amount     | Count
-------------------
00.01 JD   | 0      
00.05 JD   | 0      
00.10 JD   | 0      
00.25 JD   | 50     
00.50 JD   | 19     
01.00 JD   | 5      
05.00 JD   | 0      
10.00 JD   | 0      
20.00 JD   | 0      
50.00 JD   | 0      
__________________
Total: 27.00 JD
```

## Technologies Used
- Java 17
- Lombok

## How to Run

1. Clone the repository:
   ```sh
   git clone https://github.com/0bada02/Vending-Machine-Simulation.git
   ```
2. Navigate to the project directory:
   ```sh
   cd Vending-Machine-Simulation
   ```
3. Compile and run the program:
   ```sh
   javac -cp lombok.jar com/progressoft/samples/*.java
   java com.progressoft.samples.Main
   ```

## License

This project is open-source under the MIT License.
