# Usage

Once you have installed and configured the project, you can start using
it to automate the process of retrieving and sending daily class schedules.
Follow these steps to use the project effectively:

1. **Running the Main Module:**
    - Execute the main module ('main.py') to fetch today's class schedules 
      and send it to the specified email recipients.
      
            python main.py

2. **Monitoring and Troubleshooting:**
    - Monitor the execution of the project to ensure that class schedules 
      are fetched and sent correctly.
    - Check for any error messages in the console output.

3. **Customization:**
    - Customize the email recipients, subject, and message content as needed
      by modifying the 'main.py'.
    - View the [Code Explanation] to modify according to your needs.

4. **Automating with Cron or GitHub Actions:**
    - To automate the process of fetching and sending class schedules daily
      you can set up a cron job on your system or use GitHub Actions.
    - How to use GitHub Actions for automate the project mentioned in the
      [GitHub Actions Integration](github_actions_integration.md).