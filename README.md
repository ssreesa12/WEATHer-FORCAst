# WEATHER-FORCAST-APPLICATION

This is a Python-based console application that allows users to securely log in and view weather forecasts for a city of their choice using a weather API. The application includes user authentication, password recovery options, and a limit on login attempts. After logging in, users can input a city name to retrieve the weather forecast, including temperature, humidity, and other relevant details.

## Features
- **User Authentication:**
  - Sign-up with email and password (passwords are securely hashed).
  - Sign-in for registered users.
  - Password recovery via security question.
  - Limits login attempts (maximum of 5 before the system locks out the user).
  
- **Weather Forecast API:**
  - After a successful login, users can input a city to fetch the weather data from a weather API (e.g., OpenWeatherMap).
  - Displays current temperature, weather description, humidity, and wind speed.

- **Input Validation:**
  - Passwords must meet security standards (at least 8 characters, with an uppercase letter, lowercase letter, number, and special character).
  - Email validation ensures proper format.


## Requirements

- Python 3.x
- `bcrypt` library for password hashing
- `csv` for handling user data storage
- A weather API (e.g., OpenWeatherMap or WeatherAPI) for weather forecast functionality
- `re` module for email validation using regular expressions

## Installation

1. Clone the repository to your local machine:
    ```bash
    git clone https://github.com/ssreesa12/weather-forecast-app.git
    ```

2. Navigate to the project directory:
    ```bash
    cd weather-forecast-app
    ```

3. Install the required dependencies using `pip`:
    ```bash
    pip install bcrypt requests
    ```

4. (Optional) Set up your weather API key (if you're using a specific weather service like OpenWeatherMap):
    - Sign up for an API key at [OpenWeatherMap](https://openweathermap.org/) or any other weather API.
    - Add the API key to the weather API function.

## Usage

1. Run the **main.py** file to start the application:
    ```bash
    python main.py
    ```

2. Upon starting, the application will provide three options:
    - **Sign Up**: For new users to register.
    - **Sign In**: For existing users to log in.
    - **Forgot Password**: For users who forgot their password and want to reset it by answering their security question.

3. After a successful login, users can:
    - Enter a city name to fetch the weather forecast.
    - Choose to log out to return to the main menu.

### Example Output:
Welcome to the Weather Forecast Application!

1) Sign Up (New User)
2) Sign In (Existing User)
3) Forgot Password
Enter your choice (1, 2, or 3): 1 Enter email: user@example.com Enter password: ******** Enter a security question: What is your pet's name? Enter the answer to the security question: Fluffy Registration successful! You can now log in.

Proceeding with login...

You're logged in!

Check Weather Forecast (Coming soon)
Logout
Enter your choice (1 for weather, 2 to logout): 2 Logging out...


## Modules

- **auth.py**: Handles user sign-up, sign-in, and password recovery functions. Uses password hashing with `bcrypt` to securely store passwords.
- **validation.py**: Contains a function to validate user passwords based on security requirements.
- **email_validation.py**: Contains a function to validate email addresses using regular expressions.
- **storage.py**: Handles reading/writing user data (email, hashed password, security question/answer) to/from a CSV file.
- **main.py**: The main entry point that coordinates the user interface, calling functions from other modules as needed.

## Security

- **Password Hashing**: User passwords are hashed using the `bcrypt` library, ensuring that even if the CSV file is compromised, the passwords remain secure.
- **Login Attempts**: The application limits login attempts to 5. After 5 failed login attempts, the user will be locked out of the system until it is restarted.

## Future Features

- **Weather Forecast**: Integrate a weather API (e.g., OpenWeatherMap) to fetch and display real-time weather information based on the user's chosen city.
- **More Robust Error Handling**: Improve error handling for invalid inputs, network failures, and API errors.

## Contributing

Feel free to submit pull requests or issues for improvements and bug fixes. All contributions are welcome!

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.




