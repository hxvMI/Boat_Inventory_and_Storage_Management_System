# Boat_Inventory_and_Storage_Management_System

A C program designed to manage boat information, such as inventory, storage locations, payments, and monthly charges. This program reads from a CSV file, allows for real-time manipulation of boat data, and saves updated information back to the file.

## Features

- **Inventory Management**: Add, view, and remove boats from the system.
- **Storage Types**: Boats can be stored in slips, on land, in storage spaces, or on trailers.
- **Payments**: Process payments for individual boats, reducing their outstanding balance.
- **Monthly Charges**: Apply monthly storage fees based on the type of storage and boat length.
- **CSV File Handling**: Reads and writes boat data to/from a CSV file for persistence.

## How It Works

The program works by reading boat data from a CSV file, allowing users to interact with the data, and saving changes back to the file when the program exits.

### Place Types

The system supports different types of storage for boats:
- `slip`: Boats are stored in water slips.
- `land`: Boats are stored on land, assigned by bay letters.
- `trailor`: Boats are stored on trailers with specific license tags.
- `storage`: Boats are stored in numbered storage spaces.

## Usage

### Compilation

To compile the program, use the following command:

```bash
gcc -o BoatManagementSystem BoatManagementSystem.c
```

### Running the Program

To run the program, provide the CSV file containing the boat data as an argument:

```bash
./BoatManagementSystem BoatData.csv
```

### CSV File Format

The CSV file should follow the format below:

- `BoatName`: The name of the boat.
- `LengthInFeet`: The length of the boat in feet.
- `PlaceType`: One of `slip`, `land`, `trailor`, or `storage`.
- `PlaceInfo`: Slip number, bay letter (for land), trailer license tag, or storage space number.
- `MoneyOwed`: The outstanding amount of money owed for the boat.

### Menu Options

Once the program is running, you will be presented with the following options:

- `(I)nventory`: View all boats in the system, sorted by name.
- `(A)dd`: Add a new boat to the system.
- `(R)emove`: Remove a boat from the system.
- `(P)ayment`: Make a payment towards a boat's outstanding balance.
- `(M)onth`: Apply monthly storage charges to all boats.
- `(e(X)it`: Save all data and exit the program.

## Example

### Example CSV Input

```csv
Serenity,45,slip,23,150.00
BlackPearl,40,land,B,200.00
Nautilus,60,trailor,ABC123,300.00
DawnTreader,55,storage,12,400.00
```

### Example Output

```text
Welcome to the Boat Management System
-------------------------------------

(I)nventory, (A)dd, (R)emove, (P)ayment, (M)onth, e(X)it : I

Boat Name            Length Place Type  Place Info  Money Owed
--------------------------------------------------------------
Serenity             45     slip        #23         $150.00
BlackPearl           40     land        B           $200.00
Nautilus             60     trailor     ABC123      $300.00
DawnTreader          55     storage     #12         $400.00
```
