# web_ufd_scanner
web_ufd_scanner
# UFD Scanner Web App

A standalone MHTML web application that converts the original Python UFD scanner into a browser-based tool. This app allows users to scan folders containing ZIP/UFD files for specific device configurations and extraction status.

## Features

- **Standalone Application**: No server or installation required - runs entirely in the browser
- **Folder Scanning**: Select entire folders to scan for ZIP/UFD files
- **Advanced Filtering**: Filter by device type, extraction status, file type, and build patterns
- **Real-time Progress**: Live progress tracking with detailed status information
- **Debug Mode**: Optional detailed logging for troubleshooting
- **Results Export**: Download scan results as a detailed text report
- **Responsive Design**: Works on desktop and mobile devices

## How to Use

1. **Open the Application**: Double-click `UFD_Scanner_WebApp.mhtml` to open it in your default browser
2. **Select Folder**: Click "Choose Folder" and select a directory containing ZIP or UFD files
3. **Configure Filters** (optional):
   - **Device/OS Filter**: Filter by specific device types (Android, iPhone, Windows, etc.)
   - **Extraction Status**: Filter by extraction completeness (Full, Partial, Metadata Only, Failed)
   - **File Type**: Filter by file purpose (Backup, Image, Log)
   - **Build Filter**: Use wildcards to filter by build patterns (e.g., `2024.*` or `*debug*`)
   - **Debug Mode**: Enable for detailed logging of all scanned files
4. **Start Scan**: Click "Start Scan" to begin the analysis
5. **Monitor Progress**: Watch real-time progress and see matching files as they're found
6. **Download Results**: Click "Download Results" to save a detailed report

## Filter Examples

- **Device Filter**: Select "android" to only find Android-related files
- **Build Filter**: 
  - `2024.*` - Find files with builds starting with "2024"
  - `*debug*` - Find files containing "debug" in the name
  - `v1.2.*` - Find files with version 1.2.x
- **Status Filter**: Select "full" to only find completely extracted files

## Browser Compatibility

- **Chrome/Edge**: Full support (recommended)
- **Firefox**: Full support
- **Safari**: Partial support (folder selection may be limited)

## Technical Notes

- The app analyzes file metadata and naming patterns to determine device type and extraction status
- No actual ZIP file extraction is performed for security reasons
- All processing happens locally in your browser - no data is sent to external servers
- The app can handle folders with thousands of files efficiently

## File Analysis Logic

The scanner analyzes files based on:
- **Filename patterns**: Device type detection from naming conventions
- **File size**: Estimation of extraction completeness
- **File metadata**: Last modified dates and other properties
- **Build patterns**: Wildcard matching against filename patterns

## Security

- **Local Processing**: All file analysis happens in your browser
- **No File Upload**: Files are read locally without uploading to any server
- **Privacy Protected**: No data leaves your computer during the scanning process

## Original Python App Conversion

This web app replicates the functionality of the original Python/Tkinter UFD scanner application with the following improvements:
- No installation required
- Cross-platform compatibility
- Modern web interface
- Real-time progress tracking
- Enhanced filtering options
- Detailed result reporting

## Troubleshooting

- **No files found**: Ensure the selected folder contains ZIP or UFD files
- **Browser compatibility**: Use Chrome or Firefox for best results
- **Performance**: For very large folders (>10,000 files), consider using more specific filters
- **Folder selection issues**: Some browsers may have limitations on folder access

## Support

If you encounter any issues or need assistance, please refer to the debug mode output for detailed error information.
