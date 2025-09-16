import sys
import os
import logging

# Configure logging
logging.basicConfig(
    level=logging.INFO,
    format='%(asctime)s %(levelname)s %(message)s',
    handlers=[logging.StreamHandler()]
)

def main():
    """
    Main entry point for the script.
    """
    logging.info("Script started.")
    # TODO: Add your code here
    logging.info("Script finished.")

if __name__ == "__main__":
    try:
        main()
    except Exception as e:
        logging.error(f"An error occurred: {e}")
        sys.exit(1)
          
from flask import Flask
app = Flask(__name__)
@app.route('/')
def hello():
    return "Hello, World!"
