# Input Types in HTML5

HTML5 provides many specialized `<input>` types that offer automatic validation and better user experience. Each type has a specific purpose.

## Most common input types

### **1. Text (Plain text)**
```html
<input type="text" name="name" placeholder="Your name">
```
- Single line plain text
- Use: names, addresses, etc.

### **2. Email**
```html
<input type="email" name="email" required>
```
- Validates email format automatically
- Shows email keyboard on mobile (@)
- Use: registration, login

### **3. Password**
```html
<input type="password" name="pass" required>
```
- Hides text while typing
- Browsers can save/retrieve
- Use: login, registration

### **4. Number**
```html
<input type="number" name="age" min="18" max="120">
```
- Numbers only
- Range validation (min/max)
- Shows numeric keyboard on mobile
- Attributes: `min`, `max`, `step`

### **5. Tel (Telephone)**
```html
<input type="tel" name="phone" pattern="[0-9]{9}">
```
- Shows phone keyboard on mobile
- Doesn't validate format automatically
- Use: phone numbers

### **6. URL**
```html
<input type="url" name="website" required>
```
- Validates valid URL format
- Use: websites, links

### **7. Date**
```html
<input type="date" name="birthdate">
```
- Date picker selector
- Opens date picker in modern browsers
- Format: YYYY-MM-DD
- Attributes: `min`, `max`

### **8. Time**
```html
<input type="time" name="time">
```
- Time picker
- Format: HH:MM
- Use: schedules, bookings

### **9. Search**
```html
<input type="search" name="q" placeholder="Search...">
```
- Optimized for searches
- Some browsers show clear button (X)
- Use: search bars

### **10. Range**
```html
<input type="range" name="volume" min="0" max="100" value="50">
```
- Slider control
- Value between min and max
- Use: volume, brightness, zoom

### **11. Checkbox**
```html
<label>
  <input type="checkbox" name="accept" value="yes">
  I accept the terms
</label>
```
- Select/deselect
- Can be checked or not
- Attribute: `checked`

### **12. Radio**
```html
<label>
  <input type="radio" name="gender" value="male"> Male
</label>
<label>
  <input type="radio" name="gender" value="female"> Female
</label>
```
- Only one option can be selected
- Same `name` groups the options
- Use: choose one from several

### **13. File**
```html
<input type="file" name="document" accept=".pdf,.doc">
```
- Opens file explorer
- `accept` attribute filters extensions
- For multiple: `multiple`

### **14. Color**
```html
<input type="color" name="color" value="#FF0000">
```
- Color picker
- Returns hexadecimal value
- Use: custom themes

### **15. Hidden**
```html
<input type="hidden" name="token" value="abc123">
```
- Not shown to user
- Submitted with the form
- Use: tokens, internal IDs

## Quick reference table

| Type | Validation | Mobile Keyboard | Use |
|------|-----------|-----------------|-----|
| text | No | Text | General |
| email | Yes | Email (@) | Emails |
| password | No | Text | Passwords |
| number | Yes | Numeric | Numbers |
| tel | No | Phone | Phones |
| url | Yes | URL (.) | URLs |
| date | Yes | Date picker | Dates |
| time | No | Time | Times |
| search | No | Search | Searches |
| range | No | Slider | Ranges |
| checkbox | No | - | Multiple |
| radio | No | - | One option |
| file | No | - | Files |
| color | No | - | Colors |
| hidden | No | - | Hidden data |

## Common attributes for inputs

```html
<input 
  type="text"
  name="username"          <!-- Field name -->
  id="username"            <!-- Unique ID -->
  value="john"             <!-- Initial value -->
  placeholder="Your name"  <!-- Hint -->
  required                 <!-- Required -->
  disabled                 <!-- Disabled -->
  readonly                 <!-- Read-only -->
  autocomplete="on"        <!-- Autocomplete -->
  maxlength="50"           <!-- Max characters -->
  minlength="3"            <!-- Min characters -->
>
```

## Best practice: Always use `<label>`

```html
<!-- ✓ CORRECT -->
<label for="email">Email:</label>
<input type="email" id="email" name="email">

<!-- ✗ INCORRECT -->
Email: <input type="email" name="email">
```

Labels:
- ✅ Make the form accessible
- ✅ Increase clickable area
- ✅ Improve user experience
