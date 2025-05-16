# SDET_Project
Rain Alert project

## Deployment Steps

1. Clone the repository to your EC2 instance:
   ```
   git clone <your-repository-url>
   cd <repository-directory>
   ```

2. Install the required packages:
   ```
   pip install email-validator flask-login "flask>=2.2.0,<3.0.0" flask-sqlalchemy gunicorn flask-wtf apscheduler requests sendgrid
   ```

   Note: We're specifically installing Flask 2.x to match your EC2 environment.

3. Start the application:
   ```
   gunicorn --bind 0.0.0.0:5000 main:app
   ```

4. For production, consider setting up a systemd service or using a process manager like Supervisor to keep the application running.
