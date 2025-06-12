# Bluetooth Signal Interception using Chrome

This project is a web application that uses Chrome's Web Bluetooth API to intercept signals from Bluetooth Low Energy (BLE) devices like the Mi Scale. It captures data such as weight and impedance, then calculates and displays health metrics including BMI, body fat percentage, muscle mass, and more. The app provides a simple interface for users to input their age, height, and gender, and view real-time health data from compatible devices.

## Project Goals

- Intercept Bluetooth signals from devices like the Mi Scale using Chrome's Web Bluetooth API.
- Process captured data (weight, impedance) to compute health metrics.
- Display real-time weight and detailed health results in a user-friendly web interface.
- Support health monitoring in a browser environment without additional software.

## Tech Stack

### Frontend
- **HTML/CSS/JavaScript**: Builds the single-page web application.
- **Web Bluetooth API**: Enables Chrome to scan and receive data from BLE devices.

### Other Tools
- **Google Chrome**: Required browser with Web Bluetooth API support.
- **Git**: For version control.

## Prerequisites

- **Google Chrome**: Version 56+ with Web Bluetooth API support (enable via `chrome://flags` if needed).
- **Bluetooth Device**: A compatible BLE device like the Mi Scale (device name "MIBCS").
- **Operating System**: Windows, macOS, Linux, or Android (Chrome OS also supported).
- **Git**: For cloning the repository.

3. **Enable Web Bluetooth in Chrome**
   - Open Chrome and navigate to `chrome://flags`.
   - Search for "Web Bluetooth" and ensure it’s enabled.
   - Relaunch Chrome if prompted.

4. **Ensure Bluetooth is Enabled**
   - Turn on Bluetooth on your device.
   - Ensure the Mi Scale (or compatible device) is powered on and within range.

## Running the App


1. **Grant Permissions**
   - Chrome will prompt for Bluetooth access when you click "Start." Allow access to proceed.

2. **Interact with the App**
   - Enter your age, height (in cm), and gender in the form.
   - Click "Start" to begin scanning for the Mi Scale.
   - View real-time weight and health metrics once the device is detected.

## Usage

- **Input User Data**: Provide your age, height, and gender to enable the "Start" button.
- **Scan for Device**: Click "Start" to search for the Mi Scale (device name "MIBCS").
- **View Results**:
  - Real-time weight is displayed in kg.
  - After stabilization, health metrics (BMI, BMR, fat percentage, etc.) are computed and shown.
  - The page refreshes automatically after 30 seconds to start a new session.

## Project Structure

```
bluetooth-signal-interception/
├── index.html              # Main HTML file with inline CSS and JavaScript
├── README.md               # Project documentation
```

## Limitations and Future Improvements

- **Current Limitations**:
  - Only works in Chrome with Web Bluetooth API support.
  - Requires manual permission granting for Bluetooth access.
  - Hardcoded for Mi Scale ("MIBCS"); other devices may need code adjustments.
  - No persistent data storage; results are lost on page refresh.
- **Future Improvements**:
  - Add support for more BLE devices by modifying the device name filter.
  - Implement local storage or a backend to save user data and history.
  - Enhance UI with charts or visualizations for health metrics.
  - Add error handling for Bluetooth disconnections or unsupported browsers.

## Troubleshooting

- **"Start" Button Disabled**:
  - Ensure age and height fields are filled with positive numbers.
- **Bluetooth Scanning Fails**:
  - Verify Bluetooth is enabled on your device and the Mi Scale is in range.
  - Check Chrome’s Bluetooth permissions in browser settings.
- **"Permission Denied" Error**:
  - Allow Bluetooth access when prompted by Chrome.
  - Ensure Web Bluetooth is enabled in `chrome://flags`.
- **No Data Received**:
  - Confirm the device name is "MIBCS" or update the filter in the code.
  - Check browser console for error messages.

## Contributing

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/your-feature`).
3. Commit changes (`git commit -m 'Add your feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a Pull Request.


## Contact

For questions or feedback, open an issue on GitHub or contact the repository owner.

## Acknowledgments

- Web Bluetooth API for enabling browser-based Bluetooth communication.
- Amsoft Solutions for the project concept.
