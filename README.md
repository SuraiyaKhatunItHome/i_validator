# i_validator

A Flutter package that provides various validation utilities for email, password, phone number, OTP, and required fields. It includes predefined regular expressions and validation classes to ensure proper input validation in Flutter applications.

## Features

- **Email Validation**: Checks if an email address is properly formatted.
- **Password Validation**: Ensures passwords meet security requirements (e.g., uppercase, lowercase, number, special character, minimum length).
- **Confirm Password Validation**: Verifies that the confirmation password matches the original password.
- **Phone Number Validation**: Checks for valid phone number formats.
- **OTP Validation**: Ensures OTP codes are of the correct length.
- **Required Field Validation**: Ensures required fields are not left empty.
- **File Validation**: Checks for valid image file formats.

## Installation

Add this to your `pubspec.yaml`:

```yaml
dependencies:
  i_validator: latest_version
```

Then, run:

```sh
flutter pub get
```

## Usage

Import the package:

```dart
import 'package:i_validator/i_validator.dart';
```

### Email Validation

```dart
String? emailError = EmailValidator().validate("test@example.com");
if (emailError != null) {
  print(emailError); // "Enter valid Email"
}
```

### Password Validation

```dart
String? passwordError = PasswordValidator().validate("Test@123");
if (passwordError != null) {
  print(passwordError); // "Invalid Password"
}
```

### Confirm Password Validation

```dart
String? confirmPasswordError = ConfirmPasswordValidator(password: "Test@123")
    .validate("Test@123");
if (confirmPasswordError != null) {
  print(confirmPasswordError); // "Password doesn't match"
}
```

### Phone Number Validation

```dart
String? phoneError = PhoneNumberValidator().validate("+1234567890");
if (phoneError != null) {
  print(phoneError); // "Invalid Phone Number"
}
```

### OTP Validation

```dart
String? otpError = OtpValidator().validate("123456");
if (otpError != null) {
  print(otpError); // "Invalid OTP code"
}
```

### Required Field Validation

```dart
String? requiredFieldError = RequiredFieldValidator().validate("");
if (requiredFieldError != null) {
  print(requiredFieldError); // "Required Field Can't Be Empty"
}
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

#   i _ v a l i d a t o r  
 