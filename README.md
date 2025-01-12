Welcome to my DevOps Project on building a weather dashboard using the Open Weather API and storing data in an AWS S3 bucket

Prerequisites: An access key from the Open Weather API and AWS credentials (access key ID and secret key).

The Project structure setup in VS (Visual Studio) Code is as follows:
        
        weather-dashboard/
        src/
          __init__.py
          weather_dashboard.py
        tests/
        data/
        .env
        .gitignore
        requirements.txt
        README.md

src/: Contains the main code files for the project that is __init__.py (A special Python file that indicates a directory is a package) and weather_dashboard.py (The Python script we will run for this project.)

tests/: Used for storing test cases or scripts to validate the functionality of the main code in the source folder.

data/: Stores processed weather data to be uploaded to the S3 bucket.

.env: Used to store our environment variables.

.gitignore: Used to exclude sensitive files. (We also add the .env file to .gitignore to ensure our credentials do not get pushed to a GitHub repository) *Best Practice

requirements.txt: Contains a list of Python dependencies or libraries needed for the project.

README.md: A Markdown file that serves as the documentation or introduction to the project.

## Steps to execute this project successfully:

1. Navigate to the weather-dashboard folder.
2. Run git init to initialize a new Git repository.
3. Run git branch -M main to change your main branch name to main.
4. Run the following commands:
   echo ".env" >> .gitignore
   echo "__pycache__/" >> .gitignore
   echo "*.zip" >> .gitignore
(The above commands exclude environment variables, Python bytecode files and zip files from being tracked or pushed to a GitHub Repository)

5. Run the following commands:
   
   echo "boto3==1.26.137" >> requirements.txt

   echo "python-dotenv==1.0.0" >> requirements.txt

   echo "requests==2.28.2" >> requirements.txt
   
 ('boto3' is the AWS SDK for Python, 'python-dotenv' manages our environment variables, and 'requets' will help us make HTTP requests to the weather API.)

6. Run the following command to install the libraries and dependencies:
   
    pip intall -r requirements.txt

7. Configure your AWS Credentials with the following command:

    aws configure

8. Configure environment variables (.env) with the following commands:
   
  echo "OPENWEATHER_API_KEY=replace_with_your_api_key" >> .env
  
  echo "AWS_BUCKET_NAME=replace_with_your_bucket_name" >> .env

9. Open the weather_dashboard.py file and add the Python script.
10. Run the Python script on the terminal with the following command:

    python src/weather_dashboard.py

If you made it this far and your Python script runs successfully, congratulations to you! You are officially a DevOps Engineer!
