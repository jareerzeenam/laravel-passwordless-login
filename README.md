# Laravel Passwordless Authentication App

## Introduction

This Laravel application implements a passwordless authentication system, allowing users to register with a traditional email-password combination and subsequently logging in using a unique login link sent via email. The unique login link is valid for a limited time and can only be used once, ensuring secure and convenient access.

## Features

**User Registration:**
  - Users can register by providing their name, email, and password.

**Passwordless Authentication:**
  - After registration, users can log in without entering a password.
  - The login form only requires the user's email.

**Unique Login Links:**
  - Upon login attempt, the system generates a unique login link and sends it to the user's email.
  - The login link is valid for 10 minutes.

**Security Measures:**
  - The login link can only be used once.
  - Sessions are used to track and manage login attempts and link expiration.

## Installation

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/your-repo.git
   ```

2. **Install Dependencies:**
   ```bash
   cd your-repo
   composer install
   ```

3. **Set Up Environment Variables:**
   - Duplicate the `.env.example` file and rename it to `.env`.
   - Update the `DB_` and `MAIL_` variables with your database and mail server credentials.
   - Generate a new application key:
     ```bash
     php artisan key:generate
     ```

4. **Run Migrations:**
   ```bash
   php artisan migrate
   ```

5. **Serve the Application:**
   ```bash
   php artisan serve
   ```

6. **Access the Application:**
   Open your web browser and navigate to `http://localhost:8000`.

## Usage

1. **Register:**
   - Visit the registration page and fill in the required information.

2. **Login:**
   - Log in using only your email.

3. **Receive Login Link:**
   - Check your email for the unique login link.

4. **Click Login Link:**
   - Click on the login link within 10 minutes to access your account.

5. **Logout:**
   - Log out to invalidate the current login link.

## Additional Configuration

- **Session Lifetime:**
  - You can customize the session lifetime in the `config/session.php` file.

- **Email Configuration:**
  - Adjust email configurations in the `config/mail.php` file.

## Troubleshooting

If you encounter any issues or have questions, please check the [issue tracker](https://github.com/jareerzeenam/laravel-passwordless-login/issues) for existing problems or create a new one.

## Contributing

Feel free to contribute to the development of this application by creating issues or pull requests.

## License

This Laravel Passwordless Authentication App is open-source software licensed under the [MIT License](LICENSE).

---

This README template is a starting point; feel free to expand or modify it based on your application's specific details and requirements.
