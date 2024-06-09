```python
import requests
from bs4 import BeautifulSoup

def construct_url(make, model):
    base_url = "https://how-many-bags-fit.com/car-make"
    formatted_make = make.lower().replace(" ", "-")
    return f"{base_url}/{formatted_make}/{model}-boot-space-dimensions-luggage-capacity/"

def scrape_boot_dimensions(url):
    response = requests.get(url)
    if response.status_code != 200:
        return None

    soup = BeautifulSoup(response.text, 'html.parser')
    # Find the section containing the dimensions table
    table = soup.find('table', class_='table table-striped')
    
    if not table:
        return None
    
    dimensions = {}
    rows = table.find_all('tr')
    
    for row in rows:
        cells = row.find_all('td')
        if len(cells) == 2:
            key = cells[0].get_text(strip=True)
            value = cells[1].get_text(strip=True)
            dimensions[key] = value
    
    return dimensions if dimensions else None

def main():
    make = input("Enter the car make: ")
    model = input("Enter the car model (with dashes if necessary): ")
    
    url = construct_url(make, model)
    print(f"Fetching boot dimensions from: {url}")
    
    dimensions = scrape_boot_dimensions(url)
    
    if dimensions:
        print(f"Boot dimensions for {make} {model} (in cm):")
        for key, value in dimensions.items():
            print(f"{key}: {value}")
    else:
        print(f"Could not retrieve dimensions for {make} {model}. Please check the car make and model.")
 
if __name__ == "__main__":
    main()

```

    Enter the car make:  honda
    Enter the car model (with dashes if necessary):  honda-accord-executive-2


    Fetching boot dimensions from: https://how-many-bags-fit.com/car-make/honda/honda-accord-executive-2-boot-space-dimensions-luggage-capacity/
    Boot dimensions for honda honda-accord-executive-2 (in cm):
    A - Minimum  Width: 76.4 cm
    B - Max Height: 52.6 cm
    C - Length: rear seats folded: 186.9 cm
    D - Length: rear seats upright: 111 cm

