# Digital Clock - 3×5 Pixel Font Display

A unique digital clock implementation that displays time using a custom 3×5 pixel font across 4 blocks. Each digit is rendered using a bitmap pattern where specific numbers are highlighted to form the digit shape.

## Features

- **3×5 Pixel Font**: Each digit (0-9) is displayed using a custom bitmap pattern in a 3×5 grid
- **Real-time Updates**: Clock updates every second to show current time
- **Visual Feedback**:
  - **Inactive digits**: Dim gray (`#3a3a3a`) - barely visible
  - **Active time digits**: White (`#ffffff`) - displays current hour and minute
  - **Active seconds**: Orangered - highlights the current second value
- **4-Block Layout**: 
  - Block 1: First digit of hour (00-14)
  - Block 2: Second digit of hour (15-29)
  - Block 3: First digit of minute (30-44)
  - Block 4: Second digit of minute (45-59)

## How It Works

The clock uses a 3×5 grid system where each block contains numbers arranged in a table:
- **Row 0**: 00, 05, 10
- **Row 1**: 01, 06, 11
- **Row 2**: 02, 07, 12
- **Row 3**: 03, 08, 13
- **Row 4**: 04, 09, 14

Each digit pattern is defined as an array of data-value attributes that need to be highlighted. For example:
- Digit "1": `##. / .#. / .#. / .#. / ###`
- Digit "2": `### / ..# / ### / #.. / ###`
- Digit "8": `### / #.# / ### / #.# / ###`

## Digit Patterns

The clock uses the following bitmap patterns for each digit:

```
0: ### / #.# / #.# / #.# / ###
1: ##. / .#. / .#. / .#. / ###
2: ### / ..# / ### / #.. / ###
3: ### / ..# / ### / ..# / ###
4: #.# / #.# / ### / ..# / ..#
5: ### / #.. / ### / ..# / ###
6: ### / #.. / ### / #.# / ###
7: ### / ..# / ..# / ..# / ..#
8: ### / #.# / ### / #.# / ###
9: ### / #.# / ### / ..# / ###
```

Where:
- `#` = filled/highlighted pixel
- `.` = empty/inactive pixel

## Usage

Simply open `clock.html` in a web browser. The clock will automatically:
1. Display the current time in HH:MM format using the 4 blocks
2. Highlight the current second value in orangered
3. Update every second

## Technical Details

- **Language**: HTML, CSS, JavaScript (vanilla)
- **Font**: Rajdhani (Google Fonts)
- **Color Scheme**:
  - Background: Black (`#000`)
  - Inactive digits: Dark gray (`#3a3a3a`)
  - Active time: White (`#ffffff`)
  - Active seconds: Orangered
- **Update Frequency**: 1000ms (1 second)

## Browser Compatibility

Works in all modern browsers that support:
- CSS Flexbox
- ES6 JavaScript features (arrow functions, template literals, etc.)
- `querySelector` and `querySelectorAll`

## File Structure

```
clock.html          # Main HTML file with embedded CSS and JavaScript
README.md           # This documentation file
```

## Customization

You can customize the clock by modifying:

1. **Colors**: Edit the color values in the CSS and JavaScript sections
2. **Font**: Change the Google Fonts import and font-family
3. **Digit Patterns**: Modify the `digitPatterns` object to change how digits are displayed
4. **Update Frequency**: Change the `setInterval` value (currently 1000ms)

## License

Free to use and modify.

