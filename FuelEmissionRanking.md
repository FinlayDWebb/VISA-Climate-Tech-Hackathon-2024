```python
import pandas as pd
import os

def get_emissions_data(csv_file, make, model, year):
    try:
        # Load the dataset
        df = pd.read_csv(csv_file)
        
        # Filter the dataset based on user input
        filtered_df = df[(df['Make'] == make) & (df['Model'] == model) & (df['Year'] == int(year))]
        
        if filtered_df.empty:
            return None
        
        # Get the lowest emissions value
        min_emission = filtered_df['Emissions'].min()
        
        return min_emission
    
    except Exception as e:
        print(f"An error occurred: {e}")
        return None

# Example usage
if __name__ == "__main__":
    # Prompt the user for input
    make = input("Enter the car make: ").strip()
    model = input("Enter the car model: ").strip()
    year = input("Enter the car year: ").strip()
    
    # Path to the CSV file (relative to the current working directory)
    csv_file = 'Trim_table.csv'
    
    if not os.path.isfile(csv_file):
        print(f"CSV file {csv_file} not found. Please ensure the file is in the same directory as the script.")
    else:
        emissions = get_emissions_data(csv_file, make, model, year)
        
        if emissions is not None:
            print(f"The lowest emissions data for {make} {model} {year} is: {emissions}")
        else:
            print(f"No emissions data found for {make} {model} {year}.")

```

    Enter the car make:  abarth
    Enter the car model:  124 spider
    Enter the car year:  2016


    An error occurred: 'utf-8' codec can't decode byte 0xcf in position 12: invalid continuation byte
    No emissions data found for abarth 124 spider 2016.

