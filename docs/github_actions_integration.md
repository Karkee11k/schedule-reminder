# GitHub Actions Integration

GitHub Actions allow you to automate workflows directly within your 
GitHub repository. Here's how you can integrate the project with GitHub
Actions to automate the process of fetching and sending daile class
schedules:

1. **Create a Workflow File:**
    - Create a YAML file (e.g., 'workflow.yml') in the '.github/workflows'
      directory of your GitHub repository. 
    - Define the workflow steps to run the main module ('main.py') at the
      desired time each day.
    
    Example 'workflow.yml': 

        '''yaml
        name: Send daily class schedule

        on:
            schedule:
                - cron: '30 8 * * *' # Run every day at 8.30 am

        jobs:
            fetch-and-send-schedule:
                runs-on: ubuntu-latest

                env:  # Define environment variables
                    ME: ${{ secrets.ME }}
                    SHEET_ID: ${{ secrets.SHEET_ID }}
                    API_KEY: ${{ secrets.API_KEY }}
                    MAIL_ID: ${{ secrets.MAIL_ID }}
                    PASSWORD: ${{ secrets.PASSWORD }}
                    
                steps: 
                    - name: Checkout Repository
                      uses: actions/checkout@v2

                    - name: Set up Python
                      uses: actions/setup-python@v2
                      with:
                        python-version: '3.x'

                    - name: Install Dependencies
                      run: pip install -r requirements.txt

                    - name: Execute Main module 
                      run: python main.py
        '''

2. **Add Repository Secrets:**
    - Store sensitive information such as API keys and email passwords
      as secrets in your GitHub repository.
    - Navigate to your repository's Settings > Secrets and add the secrets.

3. **Monitor Workflow Execution:**
    - Monitor the workflow execution in the Actions tab of your GitHub
      repository.
    - Check for any failures or errors in the workflow runs.

By integrating the project with GitHub Actions, you can automate the process
of fetching and sending daily class schedules.