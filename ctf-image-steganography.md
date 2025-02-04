🕵️ Incident:

The challenge involved finding hidden information within an image file. The image appeared to be ordinary but was suspected to contain encoded data.

🔎 Investigation:

- Step 1: Downloaded the image file and ran basic analysis using binwalk to check for embedded data.
- Step 2: Found that the image contained hidden data in the least significant bits (LSB), a common technique in steganography.
- Step 3: Used the tool zsteg to extract the hidden message encoded in the image’s LSB.
- Step 4: Decrypted the extracted message, which contained a string that led us to the flag.

🛡️ Mitigation:

- Step 1: Documented the technique used and updated the team about the dangers of hidden messages in files and images.
- Step 2: Recommended using steganography detection tools in future image-based files that enter the network.
- Step 3: Created a policy to inspect files for steganography during file uploads and sharing, especially for sensitive information.
