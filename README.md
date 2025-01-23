# Microsoft Clarity Playback URL

## Overview
This repository contains a WEB Google Tag Manager (GTM) custom variable template named **Microsoft Clarity Playback URL**. This template generates session recording playback URLs for Microsoft Clarity by processing the `_clsk` and `_clck` cookies.

## How It Works
- Reads and URL-decodes `_clsk` and `_clck` cookies.
- Splits cookie values by the `|` character and extracts the first segment.
- Combines the extracted values with the Clarity Project ID to generate the playback URL.
- Returns `undefined` if any required data is missing or invalid.

## Installation
1. Import the template into your Google Tag Manager account:
   - Download the [template JSON file](https://github.com/Jude-Nwachukwu/microsoft-clarity-playback-url/blob/main/template.tpl).
   - Navigate to **Templates** > **New** > **Import Template** in GTM.
  
Alternatively, you can download the **template.tpl** file and import it to your GTM web GTM container as a variable custom template.

2. Configure the **Clarity Project ID** field with your Microsoft Clarity Project ID.

## Usage
1. Add the variable to your GTM workspace:
   - Go to **Variables** > **New** > **Choose Variable Type** > **Microsoft Clarity Playback URL**.
2. Use the variable in your GTM tags or triggers as needed.

## Example Output
Given the following:
- `_clsk` cookie value: `abcd1234|someotherdata`
- `_clck` cookie value: `xyz987|moredata`
- Clarity Project ID: `myProjectID`

The generated playback URL will be:

https://clarity.microsoft.com/player/myProjectID/xyz987/abcd1234


## Additional Resources
- Learn how to integrate session recording tools (like Microsoft Clarity) with analytics platforms such as Google Analytics, Piwik Pro, Mixpanel, and more:  
  [Read the guide here](https://dumbdata.co/post/how-to-integrate-session-recording-tools-with-your-analytics/).

- For insights and learnings on integrating GA4 with Microsoft Clarity, explore this detailed resource:  
  [Read more here](https://www.rootandbranchgroup.com/integrate-microsoft-clarity-and-google-analytics/).

## Author
Created by Jude Nwachukwu Onyejekwe.

Created as part of the [Dumbdata.co](https://dumbdata.co) measurement resource hub to provide you with resources that help simplify measurement.

## License
This project is licensed under the [License](LICENSE).
