# Terminal iMessage Sender

A simple script to send iMessages directly from your terminal.

## Requirements

- macOS  
- Messages (iMessage) set up and signed in on your Mac  
- Terminal access  

> No additional installations are required.

## Installation

1. Download the `text` script to your computer.  
2. Move it to your home directory (or any directory you prefer). Example for moving to home directory:

```bash
mv ~/Downloads/text ~/text
```

3.	Make the script executable:
```bash
chmod +x ~/text
```
## Usage

Navigate to the directory containing the script (if in home directory, cd ~). Then run:
```bash
./text CONTACT_NAME "Your message here"
```
Example:
```bash
./text "Mom" "Call you back in 10 minutes"
```
The script will send the message to the contact name provided. Make sure the contact exists in your iMessage contacts.

## Notes
- The CONTACT_NAME must match the name in your Messages app exactly.
  
- Quotes around the message are required if it contains spaces.

## Troubleshooting
- If the script doesn’t send messages, make sure Messages is running.
  
- Ensure macOS has granted Terminal permission to control Messages (check System Settings > Privacy & Security > Automation).
  
- Contact names must exactly match the iMessage contact, including capitalization.
  
- If you move the script to another directory, adjust the path accordingly when running it.
