## Stocker: Real-Time Stock Market Price Checker

**Built with:**

* Django (Backend)
* Django-Channels (WebSockets)
* Celery (Asynchronous Tasks)
* Additional Libraries (JavaScript, Bootstrap, FontAwesome, HTML/CSS)

**Project Description**

This application allows users to track stock prices in real-time without requiring login or signup. Users can select multiple stocks from a list and view their current prices that update regularly. The application leverages Django Channels and WebSockets to establish real-time communication for price updates.

**Project Features:**

* Real-time stock price updates
* User selection of multiple stocks for tracking
* Stock details view (implementation details omitted)
* Temporary user session storage using Django Sessions (implementation details omitted)

**Technologies Used:**

* **Django:** A high-level Python web framework used for efficient backend development.
* **Django-Channels:** Enables real-time communication between the application and user browsers using WebSockets.
* **Celery:** A distributed task queue that facilitates asynchronous execution of tasks, improving application responsiveness.
* **Message Broker (Memcached/Redis):** (Optional) Stores messages for real-time communication and adds a Django Channel Layer to the backend.
* **JavaScript:** Adds interactivity and functionality to the application's frontend.
* **Bootstrap 5:** Provides a robust CSS framework for responsive and visually appealing UI development.
* **FontAwesome:** Offers a collection of icons to enhance the user interface.
* **HTML/CSS:** The fundamental building blocks for creating web page structure and styling.

**Running the Application Locally**

**Prerequisites:**

* Python (version required to be specified)
* pip (package installer)

**Installation:**

1. Clone the repository.
2. Navigate to the project directory using your terminal.
3. Install required dependencies: `pip install -r requirements.txt`

**Server Startup:**

1. Open a new terminal window.
2. Start the Django development server: `python manage.py runserver` (This command might differ based on your project setup.)
3. (Optional) Start the Celery worker: `celery -A stockmarket.celery worker --pool=solo -l info`
4. (Optional) Start the Celery Beat scheduler: `celery -A stockmarket beat -l INFO`

**Note:**

* The specific commands for running the Celery worker and scheduler might vary depending on your project configuration. Refer to the Celery documentation for detailed instructions.

**Additional Notes**

* Clear the task queue if outdated stock details persist: `celery -A stockmarket purge -f`
* Consider using environment variables for sensitive information like credentials.
* Provide instructions for accessing the admin panel only if necessary for testing purposes.
