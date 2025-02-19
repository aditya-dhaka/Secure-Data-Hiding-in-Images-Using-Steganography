# Secure-Data-Hiding-in-Images-Using-Steganography

This repository demonstrates a Python implementation of image steganography, where a secret message is securely embedded within an image. The hidden message can only be accessed by users who provide the correct passcode for decryption. The project utilizes OpenCV for image processing and ensures the integrity of the hidden message while maintaining the visual appearance of the image.

Overview

Steganography is the technique of hiding secret data within a carrier medium, such as an image, to prevent unauthorized access. This project employs the least significant bit (LSB) method to hide the secret message inside the RGB values of an image's pixels. The message remains invisible to the naked eye, and access to the hidden data is secured through password protection. The message can only be retrieved by providing the correct passcode.

The program uses OpenCV to manipulate image data and enables users to securely encode and decode messages.

Features

1. Image-Based Steganography: Securely embeds a secret message into an image using pixel values.

2. Password Protection: Only authorized users with the correct passcode can decrypt the hidden message.

3. Cross-Platform Compatibility: Runs on any system with Python and OpenCV installed.

4. Preserved Image Integrity: The visual appearance of the image remains unchanged, even though the message is hidden inside the pixel data.

5. Simple Interface: User-friendly prompts for entering secret messages and passcodes.

Code Explanation

1. Message Encoding (Hiding the Message)

The script uses the least significant bit (LSB) method to hide the secret message in the image. Here's how the process works:

• The secret message is converted to its ASCII equivalent.

• The ASCII values are embedded into the least significant bits of the image's RGB channels.

• The image is modified pixel by pixel, cycling through the red, green, and blue channels to store the message.

2. Message Decoding (Retrieving the Message)

When the user provides the correct passcode for decryption:

• The program reads the least significant bits of the image's pixel values.

• It extracts the hidden message by converting the pixel values back to their ASCII equivalents.

• The decoded message is then printed.

3. Password Protection

The program requires a passcode to decrypt the hidden message. This provides an extra layer of security. If the passcode does not match the one used during encoding, the message will not be revealed.

Results

The results include the accuracy scores for all classifiers, with the XGBoost model generally performing the best. The confusion matrix for the best model is also printed for a deeper understanding of its predictions.

Here are some sample of result:

![Output2](https://github.com/user-attachments/assets/f131fab8-899c-420c-8a0b-58d5acd2cb26)

Contributing

We welcome contributions from the community. If you would like to contribute, please follow the steps below:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and test them.
4. Submit a pull request with a detailed explanation of your changes.
5. Please ensure that your code adheres to the style guide and includes relevant tests.
