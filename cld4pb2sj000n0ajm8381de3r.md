# How to use ChatGPT to web scrape EASILY

By now you have probably heard of [ChatGPT](https://chat.openai.com/chat/), the natural language processing chatbot, as it's been taking the world by storm. But did you know that ChatGPT can web scrape for you?

Let's say I am trying to web scrape [Reddit](https://old.reddit.com/r/programming/) to get a list of the post names in the subreddit [r/programming](https://www.reddit.com/r/programming/). I normally have to open up [VS Code](https://code.visualstudio.com/), start a new project, and remind myself how to use the [BeautifulSoup](https://beautiful-soup-4.readthedocs.io/en/latest/#) and [Requests](https://requests.readthedocs.io/en/latest/) libraries for web scraping. However, ChatGPT makes it easier than ever to web scrape from sites and save time. Read on for two techniques to web scrape with ChatGPT, the first one can be done fully in the browser, and the second option is more customizable.

## Steps for Technique #1: In the browser

1. First, I'll go to [a subreddit on Reddit's website](https://old.reddit.com/r/programming/). I am using the old layout because it is more accessible to web scrapers, but the content is the same.
    
2. Open up the dev tools and inspect tab by right-clicking on the page and then clicking on inspect (Keyboard shortcut: Ctrl + Shift + I on Chrome).
    
3. Then press the button below, which will allow you to hover over any element on the website and see the HTML for that element.
    
    ![How to Use Inspect select Element](https://blog.hubspot.com/hs-fs/hubfs/Google%20Drive%20Integration/How%20to%20Use%20Inspect%20Element%20In%20Chrome,%20Safari,%20and%20Firefox-Dec-11-2020-05-10-14-82-PM.png?width=1500&name=How%20to%20Use%20Inspect%20Element%20In%20Chrome,%20Safari,%20and%20Firefox-Dec-11-2020-05-10-14-82-PM.png align="left")
    
4. Then press on one of the titles, and it will highlight the HTML for that post's title.
    
    ![Pressing on a Reddit title](https://cdn.hashnode.com/res/hashnode/image/upload/v1674178783103/5f7d3e91-9ac0-4872-8399-bca25019eb70.png align="center")
    
    ![The HTML tag for the Reddit title](https://cdn.hashnode.com/res/hashnode/image/upload/v1674179015548/675cf8b5-8ef6-4b45-a036-1f64bc8bb5e7.png align="center")
    
5. Then open up [ChatGPT](https://chat.openai.com/chat/). Typing the text below will give you code that you can copy and paste into the console tab of the dev tools. Feel free to change the tag type and class name based on what you are trying to scrape.
    
    `I want to extract posts from a website. The posts are in an <a> tag with the class names "title may-blank". Give me JS code that will extract the first 25 posts and put it in an excel file. I want to run this code in the browser console.`
    
    ![ChatGPT response with the code](https://cdn.hashnode.com/res/hashnode/image/upload/v1674179323108/2aa186a1-d795-48b8-917a-49437d63e62b.png align="center")
    
6. After a few seconds, the list of the Reddit titles downloads to your computer!
    
    ![The download box](https://cdn.hashnode.com/res/hashnode/image/upload/v1674179458640/ca37550b-de09-4ab8-b325-afcbcc72fc94.png align="center")
    

![The exported CSV file](https://cdn.hashnode.com/res/hashnode/image/upload/v1674181065118/c361edf4-284a-4ce5-b743-0f5d21c33ee3.png align="center")

This technique is possible without leaving the browser and works great for beginner projects, but is relatively limited when it comes to web scraping. However, ChatGPT can also web scrape with popular libraries like [BeautifulSoup](https://beautiful-soup-4.readthedocs.io/en/latest/#), you just have to ask. This is a little more complicated, but much more customizable.

## Steps for Technique #2: Python and BeautifulSoup

1. If you type this in [ChatGPT](https://chat.openai.com/chat/), it will give you Python code:
    
    `web scrape data from` [`https://old.reddit.com/r/programming/`](https://old.reddit.com/r/programming/) `using python and beautifulsoup`
    
    ![ChatGPT response with the code](https://cdn.hashnode.com/res/hashnode/image/upload/v1674182628925/95ab7cc2-ffb2-45e1-9fdf-dc8bbb49a459.png align="center")
    
2. Open up an IDE or code editor (I use VS Code), make a new Python file and paste the code in.
    
3. Sometimes Reddit blocks the request if you try too many requests, so it is a good practice to add your user agent to the headers of the request. User agents help website servers identify where your request is coming from, which makes it less likely to get blocked. Luckily, ChatGPT can help with this too!
    
4. Asking ChatGPT to add user agents to this beautifulsoup and python code returns the code with this as an update:
    
    `headers = { 'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/89.0.4389.82 Safari/537.36'}`
    
    `requests.get("`[`https://old.reddit.com/r/programming/`](https://old.reddit.com/r/programming/)`", headers=headers)`
    
5. Run the full code, and in the terminal, you see the scraped information!
    
    ![Code with the Reddit titles, post creator names, and number of comments printed out](https://cdn.hashnode.com/res/hashnode/image/upload/v1674182836585/e7ef9a74-2e9e-4b22-814f-a044d70af42b.png align="center")
    
6. One thing you might notice is that the code scrapes the title names, in addition to the user who posted it and the number of comments it has. To get only the titles, you can ask ChatGPT this:
    
    `web scrape only the post titles from` [`https://old.reddit.com/r/programming/`](https://old.reddit.com/r/programming/) `using python and beautifulsoup`
    
7. Now, to save it to a CSV file, just ask ChatGPT to `update this code to save the title names in a csv file after running.`
    
8. Quick note, make sure to change the folder that you are in inside of your terminal, because that is where the CSV file will be created. To do this, use the [cd command](https://www.howtogeek.com/666127/how-to-use-the-cd-command-on-linux/).
    
9. After pasting the new code in, a CSV file will be added to your folder, and it contains all the article names!
    
    ![Final CSV file](https://cdn.hashnode.com/res/hashnode/image/upload/v1674184084430/342045bb-714f-45ed-9187-bede9b78a5ed.png align="center")
    

## Final Code

Here is the final code:

> ```python
> import requests
> from bs4 import BeautifulSoup
> import csv
> 
> headers = {
>     'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/89.0.4389.82 Safari/537.36'
> }
> 
> # Make a request to the website
> response = requests.get("https://old.reddit.com/r/programming/", headers=headers)
> 
> # Parse the HTML content
> soup = BeautifulSoup(response.content, "html.parser")
> 
> # Find all the elements with the class "title"
> post_titles = soup.find_all("a", class_="title")
> 
> # Extract the text from the elements
> titles = [title.get_text() for title in post_titles]
> 
> # Save the titles in a CSV file
> with open('titles.csv', mode='w') as csv_file:
>     fieldnames = ['title']
>     writer = csv.DictWriter(csv_file, fieldnames=fieldnames)
>     writer.writeheader()
>     for title in titles:
>         writer.writerow({'title': title})
>         
> print("Titles saved in titles.csv file")
> ```

If you would like to add any more functionality, all you have to do is just ask ChatGPT using these same steps.

## Conclusion

These techniques are super powerful and can save you a lot of time when scraping websites. A few years ago, I coded a web scraping project that took me hours and hours to finish, but if I tried to redo it now, it would take drastically less time because of ChatGPT.

Comment below what you think about coding with ChatGPT!