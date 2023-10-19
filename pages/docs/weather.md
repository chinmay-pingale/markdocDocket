# Weather API  Documentation

Automated with **Ducks** 





# Introduction

Welcome to the Weather API  documentation made by IDP 2023. This documentation will guide you through the usage of the API, including a sandbox, header descriptions, curl commands, and more.

**Developer Name:** Chinmay

**Developer Email:** cp@gmail.com

**API Name:** Weather API 

**API Use Case:** Gives weather for a specific location

**Additional Relevant Info:** 
# Endpoints 

## Endpoint: `https://api.weather.gov/gridpoints/TOP/31,80/forecast`
### `GET` METHOD 
### Attributes:
--- 
### Calling the API:
>```curl https://api.weather.gov/gridpoints/TOP/31,80/forecast```


<details><summary>Python</summary><br><pre><code>import requests

url = 'https://api.weather.gov/gridpoints/TOP/31,80/forecast'
headers = {}
data = None
response = requests.get(url, headers=headers, data=data)

if response.status_code == 200:
    print('Request was successful!')
    print('Response content:', response.text)
else:
    print(f'Request failed with status code: {response.status_code}')
    print('Response content:', response.text)
</code></pre></details><details><summary>TypeScript</summary><br><pre><code>import axios from 'axios';

const url = 'https://api.weather.gov/gridpoints/TOP/31,80/forecast';
const headers = {};
const data = null;
axios.get(url, {},
})
.then((response) => {
    if (response.status === 200) {
        console.log('Request was successful!');
        console.log('Response content:', response.data);
    } else {
        console.error(`Request failed with status code: ${response.status}`);
        console.error('Response content:', response.data);
    }
})
.catch((error) => {
    console.error('An error occurred:', error);
});
</code></pre></details><details><summary>C#</summary><br><pre><code>using System;
using System.Net.Http;

var httpClient = new HttpClient();

var request = new HttpRequestMessage(new HttpMethod("GET"), "https://api.weather.gov/gridpoints/TOP/31,80/forecast");

var response = await httpClient.SendAsync(request);

if (response.IsSuccessStatusCode)
{
    var content = await response.Content.ReadAsStringAsync();
    Console.WriteLine("Request was successful!");
    Console.WriteLine("Response content: " + content);
}
else
{
    Console.WriteLine("Request failed with status code: " + (int)response.StatusCode);
    var content = await response.Content.ReadAsStringAsync();
    Console.WriteLine("Response content: " + content);
}
</code></pre></details>

--- 
### Output:
>```None```