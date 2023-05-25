# Goal
The Mailing List Summarizer is a project aimed at creating an updated feed for public consumption by summarizing daily threads from the Bitcoin and Lightning Development mailing lists. The project utilizes a cronjob to scrape the [bitcoin-dev](https://lists.linuxfoundation.org/pipermail/bitcoin-dev) and [lightning-dev](https://lists.linuxfoundation.org/pipermail/lightning-dev) mailing lists and generate summaries. The summaries will be pushed to the [mailing-list-summaries](https://github.com/urvishp80/mailing-list-summaries) repository using GitHub action.
### Project Setup
1. Install all the dependencies from requirements.txt file: `pip install -r requirements.txt`
2. Set up environment variables: Create `.env` file in the root folder and add following keys -
    ```
   OPENAI_API_KEY="<your_api-Key>"
   ES_CLOUD_ID = "<your_es_cloud_id>"
   ES_USERNAME = "<your_es_username>"
   ES_PASSWORD = "<your_es_password>"
   ES_INDEX = ""<your_es_index>""
   ```
3. You can run externally by using this command: `python xmls_generator_production.py` otherwise it will run daily at 12:00 am UTC using GitHub actions(yml file present in .github/workflows)

