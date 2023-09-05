# ASSIGNMENT-2-
Nimesa Technology Pvt. Ltd


   

  import requests


API_URL = "https://samples.openweathermap.org/data/2.5/forecast/hourly?q=London,us&appid=b6907d289e10d714a6e88b30761fae22"

def get_temperature(data, date_time):
    for entry in data:
        if entry['date_time'] == date_time:
            return entry['temperature']
    return None

def get_wind_speed(data, date_time):
    for entry in data:
        if entry['date_time'] == date_time:
            return entry['wind']['speed']
    return None


def get_pressure(data, date_time):
    for entry in data:
        if entry['date_time'] == date_time:
            return entry['pressure']
    return None


def main():
    while True:
        print("\nMenu:")
        print("1. Get Temperature")
        print("2. Get Wind Speed")
        print("3. Get Pressure")
        print("0. Exit")

        choice = input("Enter your choice: ")

        if choice == '1':
            date_time = input("Enter the date and time (YYYY-MM-DD HH:MM): ")
            temperature = get_temperature(data, date_time)
            if temperature is not None:
                print(f"Temperature at {date_time}: {temperature}°C")
            else:
                print("Data not available for the specified date and time.")
        elif choice == '2':
            date_time = input("Enter the date and time (YYYY-MM-DD HH:MM): ")
            wind_speed = get_wind_speed(data, date_time)
            if wind_speed is not None:
                print(f"Wind Speed at {date_time}: {wind_speed} m/s")
            else:
                print("Data not available for the specified date and time.")
        elif choice == '3':
            date_time = input("Enter the date and time (YYYY-MM-DD HH:MM): ")
            pressure = get_pressure(data, date_time)
            if pressure is not None:
                print(f"Pressure at {date_time}: {pressure} hPa")
            else:
                print("Data not available for the specified date and time.")
        elif choice == '0':
            print("Exiting program.")
            break
        else:
            print("Invalid choice. Please enter a valid option.")


if __name__ == "__main__":

    data = [
        {"date_time": "2019-03-30 12:00", "temperature": 278.76, "wind": {"speed": 5.2}, "pressure": 1021.88},

    ]
    main()



