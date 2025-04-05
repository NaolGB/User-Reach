# User-Reach

A tool for targeted outreach to potential Meetup group members using AI-generated personalized messages.

## Overview

User-Reach helps Meetup organizers grow their communities by:

1. Scraping member data from existing Meetup groups
2. Parsing and analyzing member profiles
3. Generating personalized invitation messages using OpenAI GPT models
4. Creating direct message links for efficient outreach

## Features

-   HTML to JSON parsing of Meetup member lists
-   Personalized message generation with OpenAI GPT models
-   Member data extraction including join date and activity level
-   AB testing of different message templates
-   Export functionality for message campaigns

## Requirements

-   Python 3.7+
-   OpenAI API key

## Setup

1. Clone this repository
2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3. Set up your OpenAI API key as an environment variable:
    ```bash
    export OPENAI_API_KEY="your-api-key-here"
    ```

## Usage

1. **Collect HTML content**: Copy the HTML content from a Meetup group's members page. To extract the outer HTML in most browsers:
    - Right-click on the members list section and select **Inspect** or **Inspect Element**.
    - In the developer tools, right-click on the highlighted HTML element and choose **Copy** > **Copy outerHTML**.
    - Paste the copied HTML into a text editor or directly into the appropriate cell in the notebook.

2. **Run the Jupyter notebook**: Open and run `create_message_meetup.ipynb`.
3. **Paste the HTML**: Add the HTML content to the appropriate cell
4. **Configure group information**:
    - Set your target group name
    - Set the source group name
    - Add your event link
    - Set your name as organizer
5. **Run the notebook**: Generate personalized messages for each member
6. **Export results**: The notebook will create a CSV file with member info and personalized messages

## Workflow Example

1. Find a related Meetup group whose members might be interested in your event
2. View the members page and save the HTML content
3. Run the notebook to generate personalized messages
4. Use the generated message links to contact members through Meetup's messaging system

## Message Customization

The tool supports multiple message templates for A/B testing. You can modify the existing templates or add your own in the `get_message()` function.

## Privacy & Ethics

-   Always follow Meetup's terms of service
-   Be respectful of members' privacy
-   Don't spam - ensure your messages are relevant and valuable
-   Respect rate limits when sending messages

## License

MIT License

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
