# GPO Glossary Website

A beautiful, responsive glossary website for the Global Partners Organization that displays business terms and definitions in an organized, searchable format.

## Features

- **Alphabetical Navigation**: Browse terms by clicking on letters A-Z
- **Search Functionality**: Search across term names, definitions, and other fields
- **Expandable Term Cards**: Click on any term to see detailed information
- **Organized Information**: Terms are organized into 4 logical categories:
  - Clear and Concise Business Definitions
  - Ownership and Stewardship
  - Relationships and Hierarchy
  - Governance Information
- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **No Database Required**: All data is embedded in the HTML file

## Files

- `index.html` - The main glossary website
- `csv-to-glossary.html` - Data conversion tool for Google Sheets
- `README.md` - This documentation file

## How to Use

### Option 1: Quick Start (for testing)
1. Open `index.html` in your web browser
2. The site will load with sample data to show you how it works

### Option 2: Add Your Own Data
1. Open your Google Sheet with glossary data
2. Open `csv-to-glossary.html` in your web browser
3. Follow the instructions to convert your data
4. Update `index.html` with your converted data
5. Open `index.html` to see your glossary

## Google Sheets Setup

Your Google Sheet should have these columns (in any order):

| Column Name | Description |
|-------------|-------------|
| Term Name | The standardized business term |
| Acronyms & Abbreviations | Common abbreviations (comma-separated) |
| Partner Owned | Whether the term is partner-owned (Yes/No) |
| Business Definition | Clear explanation of the term |
| Business Context/ Purpose | Why the term is important |
| Synonyms | Alternative names (comma-separated) |
| Business Rules | Rules governing the term's use |
| Examples of Usage | Real-world examples |
| Business Owner | Person/department responsible |
| Data Steward | Person/team maintaining the definition |
| Related Business Terms | Related terms (comma-separated) |
| Parent Terms | Higher-level terms (comma-separated) |
| Child Terms | More specific terms (comma-separated) |
| Last Reviewed Date | When last reviewed (YYYY-MM-DD format) |
| Approval Status | Current approval status |

## Updating Your Data

### Step-by-Step Process:

1. **Export from Google Sheets**:
   - Select all your data (including headers)
   - Copy it (Ctrl+C or Cmd+C)

2. **Convert the Data**:
   - Open `csv-to-glossary.html` in your browser
   - Paste your data into the text area
   - Click "Convert to JSON"
   - Copy the generated JavaScript code

3. **Update the Website**:
   - Open `index.html` in a text editor
   - Find the line that starts with `const glossaryData = [`
   - Replace the entire array with your new data
   - Save the file

4. **View Your Updates**:
   - Open or refresh `index.html` in your browser
   - Your new terms should appear

## Hosting the Website

### Local Hosting (for development/testing):
Simply open `index.html` in your web browser.

### Web Hosting:
Upload `index.html` to any web server. Popular options include:
- GitHub Pages (free)
- Netlify (free tier available)
- Vercel (free tier available)
- Your organization's web server

## Customization

### Changing Colors/Branding:
Edit the CSS variables in the `<style>` section of `index.html`:
- Primary color: `#667eea` (used for headers, buttons)
- Secondary color: `#764ba2` (used in gradients)
- Background: `#f8f9fa`

### Adding New Fields:
1. Add the field to your Google Sheet
2. Update the conversion tool if needed
3. Modify the JavaScript functions in `index.html` to display the new field

## Troubleshooting

### Common Issues:

**Terms not showing up:**
- Check that your data has the correct column headers
- Ensure Term Name field is not empty
- Try using the conversion tool to check data format

**Search not working:**
- Make sure JavaScript is enabled in your browser
- Check browser console for errors

**Layout issues on mobile:**
- The site is responsive, but complex data might need scrolling
- Consider simplifying long text fields for mobile users

**CSV conversion errors:**
- Make sure your data doesn't have special characters in unexpected places
- Try copying smaller batches if you have a very large dataset

### Browser Compatibility:
- Chrome (recommended)
- Firefox
- Safari
- Edge
- Internet Explorer 11+ (with limitations)

## Technical Details

- **Framework**: Vanilla HTML/CSS/JavaScript (no dependencies)
- **Data Format**: JSON embedded in JavaScript
- **Responsive**: CSS Grid and Flexbox
- **Icons**: Unicode emojis (no external fonts needed)
- **Search**: Client-side text matching
- **File Size**: Approximately 2-3KB + your data

## Support

For issues or questions:
1. Check this README file
2. Review the sample data format
3. Try the conversion tool with a small dataset first
4. Check browser developer console for error messages

## Future Enhancements

Potential improvements that could be added:
- Export functionality (PDF, CSV)
- Advanced filtering options
- Term cross-linking
- Version history tracking
- Bulk edit capabilities
- Analytics integration