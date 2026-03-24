# NewLine-Cinema-using-a-client-server-architecture.
The server manages a SQLite database containing information about 7 movies currently showing
Overview

The NewLine Cinema Management System is a comprehensive client-server application designed to manage cinema operations as well as movie scheduling,
ticket sales, and inventory management. The system uses a client-server architecture with socket-based communication and provides a user-friendly GUI
for cinema staff.

System Architecture

 Client-Server Model
- Server: Manages SQLite database operations and handles multiple client connections
- Client: Provides Tkinter-based GUI for user interactions
- Communication: JSON-based message protocol over TCP sockets
- Database: SQLite database with relational tables for movies and sales


Technologies Used
Backend Technologies
- Python 3.x: Core programming language and code ran in jupyter notebook 
- SQLite3: Lightweight database for data persistence
- Socket Programming: TCP socket communication between client and server
- Threading: Multi-threaded server to handle concurrent client connections
- JSON: Data serialization for client-server communication
- Logging: Comprehensive logging for debugging and monitoring

 Frontend Technologies
- Tkinter: Python's standard GUI toolkit for the client interface
- ttk (Themed Tkinter): Enhanced widgets with modern styling
- Custom Styling: Professional color scheme and layout design


Supported Actions
1. `get_movies` - Retrieve all movies
2. `add_movie` - Add a new movie
3. `update_movie` - Update existing movie details
4. `delete_movie` - Remove a movie
5. `update_tickets` - Update available ticket count
6. `record_sale` - Process ticket purchase

Key Features

Server Features
- Multi-threaded Architecture: Handles multiple concurrent client connections
- Database Management: Complete CRUD operations on movies and sales
- Error Handling: Comprehensive error handling with detailed logging
- Data Validation: Server-side validation for all database operations
- **Transaction Safety**: Atomic operations for ticket purchases
- **Auto-initialization**: Automatic database setup with sample data

Client Features
- Intuitive GUI: Professional Tkinter interface with tabbed layout
- Real-time Updates: Dynamic calculation of totals and inventory updates
- Receipt Generation: Automatic receipt creation and file saving
- Input Validation: Client-side validation before server communication
- Error Display: User-friendly error messages and status updates
- Responsive Design: Clean, organized layout with proper spacing

 Functional Components
Ticket Purchase System
- Movie selection from the dropdown list
- Real-time movie details display
- Customer information input
- Dynamic total calculation
- Ticket availability validation
- Receipt generation and storage

Movie Management System
- Add new movies with full validation
- Update existing movie details
- Delete movies with confirmation
- Real-time inventory management
- Cinema room conflict prevention

Security and Validation
- Input sanitization on both client and server
- Database constraints enforcement
- Business rule validation (room occupancy, ticket availability)
- Error handling at multiple levels

 Running the System
1. Start the Server:
   ```bash
   python cinema_server.py
   ```
   The server will create the database and populate sample data automatically.

2. Start the Client:
   ```bash
   python cinema_client.py
   ```
   The client will connect to the server automatically.

Usage Instructions

For Cinema Staff (Client Application)
Ticket Purchase Process
1. Select the "Ticket Purchase" tab
2. Choose a movie from the dropdown menu
3. Review movie details (room, dates, availability, price)
4. Enter customer name
5. Specify the number of tickets desired
6. Review the calculated total
7. Click "Purchase Tickets"
8. the Receipt is automatically generated and saved

 Error Handling
Server-Side Error Handling
- Database connection errors
- SQL constraint violations
- Invalid data format handling
- Client disconnection management
- Concurrent access protection

Client-Side Error Handling
- Network connection failures
- Invalid user input validation
- Server communication timeouts
- File system errors (receipt generation)
- GUI component error recovery


 Security Features
 Data Protection
- Input validation at multiple layers
- SQL injection prevention through parameterized queries
- Business logic enforcement in database constraints
- Error message sanitization

Future Enhancement Possibilities
Potential Improvements
- User authentication and role-based access
- Advanced reporting and analytics
- Integration with payment processing
- Mobile application interface
- Real-time notifications
- Advanced scheduling features


Troubleshooting Guide

Common Issues

Server Won't Start
- Check if port 12345 is already in use
- Verify file permissions for database creation
- Ensure Python has network access permissions

Database Errors
- Check disk space availability
- Verify database file permissions
- Review data validation requirements

Receipt Generation Issues
- Ensure write permissions in application directory
- Check available disk space
- Verify receipt directory creation

Conclusion

The NewLine Cinema Management System provides a robust, scalable solution for cinema operations management. With its clean architecture, comprehensive error handling, and user-friendly interface, it serves as an effective tool for managing movie schedules, ticket sales, and customer transactions. The system's modular design allows for future enhancements while maintaining stability and reliability in daily operations.
