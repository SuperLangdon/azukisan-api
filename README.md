

# Azukisan API - a simple web API for randomly fetching adorable Azukisan images

EN | [简体中文](https://github.com/SuperLangdon/azukisan-api/README_CN.md)

## Introduction

"Siamese Cat Azuki Is the Center of the World" (シャム猫あずきさんは世界の中心) is a work created by the Japanese manga artist Nobeko. In the story, Azukisan, the Siamese cat, is the author's pet, and it often acts spoiled towards its owner, likes to monopolize attention, and even gets jealous of others. Azukisan's behavior often leads to hilarious events, and the manga includes its wonderful and adorable actions, such as liking rain but not baths, liking grilled saury fish but not eating canned saury for cats, and so on. This work is deeply loved by cat enthusiasts, and it has inspired a lot of derivative content and fan creations revolving around the character "Siamese Cat Azuki."

<img src="https://cdn.jsdelivr.net/gh/SuperLangdon/image-hosting/202306161507360.webp" alt="World Revolves Around Cats: Azuki-san, the Siamese Cat, is the Center of the World" width="25%" />

This API is based on these works.

## Copyright

The images used in this API are sourced from the work "Siamese Cat Azuki Is the Center of the World" (もっとシャム猫あずきさんは世界の中心) created by the Japanese manga artist Nobeko, along with its fan creations. The copyright for the original work and its related fan creations belongs to Nobeko and the relevant parties involved in the fan creations.

## Purpose

When you request this API, it will randomly return a picture related to Azuki-san, the Siamese cat.

## Basic Information

Base URL: https://api.example.com/azukisan

Request Method: GET

Response Format: JSON

## Parameters

| Field  | Description                                   |
| ------ | --------------------------------------------- |
| type   | 302 (default)<br>json (supports CORS)         |
| site   | Under construction, support not yet completed. |
| size   | large (large-sized image, resolution 500*500 and above)<br>small (small-sized image, resolution 500*500 and above)<br>all (all) - (default) |
| proxy  | 1 (use reverse proxy) - (default)<br>0 (302 returns the source link) |
| tag    | No default value<br>Filter images by specified categories.<br>Under construction, support not yet completed. |

## Error Handling
When an API request fails, it will return the appropriate HTTP status code and error message.

| HTTP Status Code | Error Message                                    |
| ---------------- | ----------------------------------------------- |
| 400              | Invalid request or missing required parameters. | 
| 404              | The requested resource does not exist.          |
| 500              | The server encountered an error.                |

## Response Example

```python
import requests

base_url = "https://api.example.com/azukisan"

# Set request parameters
params = {
    "type": "302",
    "size": "large",
    "proxy": "1",
    "tag": ""
}

# Send a GET request
response = requests.get(base_url, params=params)

# Get JSON response content
json_data = response.json()

# Handle the returned JSON data
print(json_data)

```