# Terminal iMessage Sender

A simple script to send iMessages directly from your terminal.

## Requirements

- macOS  
- Messages (iMessage) set up and signed in on your Mac  
- Terminal access  

> No additional installations are required.

## Installation

1. Download the `text.txt` script to your computer.  
2. Move it to your home directory (or any directory you prefer). While doing so, get rid of the .txt extension. Example for moving to home directory:

```bash
mv ~/Downloads/text.txt ~/text
```

3.	Make the script executable:
```bash
chmod +x ~/text
```

4. Install fzf for interactive selection:
```bash
brew install fzf
```
## Usage

Navigate to the directory containing the script (if in home directory, cd ~). Then run:
```bash
./text CONTACT_NAME "Your message here"
```
Note: CONTACT_NAME is not case sensitive
Examples:
1. Single-word contact name & message (no quotes needed)
```bash
./text mom ttyl
```

2. Multi-word contact name & message (quotes required)
```bash
./text "Peter Parker" "Call you back soon"
```
If you omit the quotes when a name contains a space, the script will treat it as two separate arguments and fail.
Sample terminal output for the above command:
```bash
Sending iMessage to 'Peter Parker'…
Message successfully sent to 'Peter Parker'.
```
3. Partial name match with multiple results (not case-sensitive)
If you type only part of a name, the script will search for contacts containing that string.
```bash
./text Matthew "Game night at 8?"
```
If multiple contacts match, you'll see an interactive menu
```bash
Multiple contacts found. Use ↑/↓ to navigate, Enter to select, or ESC to cancel.
> Matthew McConaughey | +1 (555) 101-2222
  Matthew Stafford     | +1 (555) 303-4444
  Matthew Dellavedova  | +1 (555) 505-6666
  Cancel
```
- Use the arrow keys to highlight the correct contact.
- Press Enter to send the message.
- Press ESC or select Cancel to abort.
## Notes
- Quotes around the message are required if and only if it contains spaces.
  
- If fzf is not installed, the script will print all matches and exit—you’ll need to rerun with a more specific name (something that doesn't overlap with another contact).
  
- Contacts without a phone number cannot receive iMessages; the script will notify you if this is the case.
## Troubleshooting
- If the script doesn’t send messages, make sure Messages is running.
  
- Ensure macOS has granted Terminal permission to control Messages and Contacts (check System Settings > Privacy & Security > Automation).
  
- Double-check that the contact exists in your Contacts app.
  
- If you move the script to another directory, adjust the path accordingly when running it.
