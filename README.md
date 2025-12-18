================================================================================
                     LINX GATEWAY - INSTALLATION GUIDE
================================================================================

Version: 1.0.0
Application: Linx Gateway - Production Console for Linx CIJ Printers


================================================================================
                            QUICK START
================================================================================

1. Extract "Linx-Gateway-Portable-1.0.0.zip" to any folder
   (e.g., C:\LinxGateway or Desktop)

2. Double-click "Linx Gateway.exe" to run the application

3. No installation required - runs directly!


================================================================================
                       SYSTEM REQUIREMENTS
================================================================================

- Operating System: Windows 10 or Windows 11 (64-bit)
- Memory: 4 GB RAM minimum
- Disk Space: 200 MB
- Network: Ethernet connection to Linx printer


================================================================================
                      PRINTER CONFIGURATION
================================================================================

1. Launch the application

2. Click "Printer Setup" in the sidebar

3. Enter your printer settings:
   - Printer IP Address: Your Linx printer's IP (e.g., 192.168.1.100)
   - Printer Port: 29043 (default RCI port)
   - Checksum: Enabled (recommended)

4. Click "Test Connection" to verify communication

5. If successful, you'll see "Connected" status on the Dashboard


================================================================================
                         USING THE APP
================================================================================

DASHBOARD:
- View real-time printer status (Jet State, Print State)
- Start/Stop Jet and Print operations
- Monitor errors and recent activity

PRINTER SETUP:
- Configure printer IP and port
- Test connection to printer
- Save settings

PRODUCTION:
- Load print messages (templates)
- Configure print mode and buffer settings
- Send remote field data (variable data)

JOBS:
- View and manage print jobs
- Monitor job progress
- Start/Stop/Delete jobs

LOGS:
- View system activity logs
- Filter by log level
- Export logs for troubleshooting


================================================================================
                       TROUBLESHOOTING
================================================================================

CANNOT CONNECT TO PRINTER:
1. Verify the printer IP address is correct
2. Check that the printer is powered on
3. Ensure the PC and printer are on the same network
4. Verify port 29043 is not blocked by firewall
5. Try pinging the printer: ping [printer-ip]

APPLICATION WON'T START:
1. Right-click "Linx Gateway.exe" and select "Run as administrator"
2. If Windows SmartScreen appears, click "More info" then "Run anyway"
3. Check that all files were extracted (not just the .exe)

JET WON'T START:
1. Check printer status for errors
2. Verify ink and solvent levels
3. Use "Clear Error" if error state is shown

PRINT NOT WORKING:
1. Ensure Jet is running first
2. Load a valid message template
3. Configure print mode before starting print


================================================================================
                     WINDOWS FIREWALL NOTE
================================================================================

The application needs to communicate with Linx printers over TCP port 29043.
If prompted by Windows Firewall:

1. Click "Allow access"
2. Check "Private networks" at minimum
3. Click "OK"

Or manually add firewall rule:
- Program: Linx Gateway.exe
- Port: 29043 (Outbound TCP)


================================================================================
                          SUPPORT
================================================================================

For technical support or bug reports, contact your system administrator.

Linx Printer RCI Protocol Reference:
- Default Port: 29043
- Frame Format: ESC-STX-CMD-DATA-ESC-ETX-CHECKSUM
- Checksum: 2's complement of modulo-256 sum


================================================================================
                     FILES IN THIS PACKAGE
================================================================================

Linx Gateway.exe      - Main application executable
resources/            - Application resources
locales/              - Language files
*.dll                 - Required runtime libraries
LICENSE.*.txt         - License information


================================================================================
                        VERSION HISTORY
================================================================================

v1.0.0 (Initial Release)
- Dashboard with real-time printer status
- Printer connection and configuration
- Jet and Print control
- Message loading
- Remote field data management
- Print mode configuration
- Job management
- System logs with filtering and export


================================================================================
