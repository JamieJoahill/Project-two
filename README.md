
# Project 2 - Rapid Games

![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641902821/ReadMe%20images/Project%202%20-%20Rapid%20Games/rghome_inn2yn.png)




## Overview

Group Members: Oliver Skjevesland, Jamie Joahill

This was paired and it was the second project built at General Assembly. We had 48 hours to complete this application. 

## Brief

* Consume a public API.
* Have several components.
* The app can include a router with several components/pages.
* Include wireframes - that you designed before building the application.
* Be deployed online and accessible to the public.

## Deployment

[Deployed project link](https://rapidgames.netlify.app)
## Time frame

48 Hours
## Tech Stack


| Front-end | Version control | Other tools | Deployment |
|:----------| :-----------| :-------------| :---- |
| JavaScript | Git | Google dev tools | Netlify |
| React | GitHub | Insomnia |
| React Router | | VS Code live share |
| Axios |
| CSS |
| Bulma |

## Planning

We first agreed that we needed to find an API that would give us back a lot of data to work with. After looking through various different API’s we found the free games API on rapidAPI. This not only gave us a substantial amount of data to work with but it was something we were both excited to create as we were both gamers. 

After finding the freegames API we looked at the data we were getting back, and we asked ourselves as a user what we would like this application to do. We came up with the following:

* See a random game recommendation. 
* View a list of all the games.
* Search for a game.
* Filter games by genre or platform.
* Add games to a favourite section. 


**We then decided on the following features:**

* Search / filter functionality.
* Browse all games.
* Show a random game from the collection.
* Create a list of games a user could add to their collection.

Using Figma to create wireframes - We then moved on to designing the applications wireframes to help give us a better understanding of how the functionality of the app would look. We wanted to keep the design simple and clean and let the application's features shine through.

![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641902821/ReadMe%20images/Project%202%20-%20Rapid%20Games/wireframes_fimohd.png)

## Visuals

![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641902821/ReadMe%20images/Project%202%20-%20Rapid%20Games/rghome_inn2yn.png)

![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641902821/ReadMe%20images/Project%202%20-%20Rapid%20Games/rgsearchfilter_apnpbn.png)

![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641902820/ReadMe%20images/Project%202%20-%20Rapid%20Games/mygamesactive_search_pbdedj.png)

![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641902821/ReadMe%20images/Project%202%20-%20Rapid%20Games/mygamesempty_ydslfa.png)

![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641902820/ReadMe%20images/Project%202%20-%20Rapid%20Games/mygamesactive_xjdatw.png)


## Build

My implementation of search and filter: 

![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641902820/ReadMe%20images/Project%202%20-%20Rapid%20Games/filtergames_cisejr.png)

![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641902820/ReadMe%20images/Project%202%20-%20Rapid%20Games/filterfunctions_hadmuf.png)

![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641902821/ReadMe%20images/Project%202%20-%20Rapid%20Games/searchinput_lcgt8k.png)


**How I implemented myGames list within local storage:**

Using local storage was the best option to implement a collection of games that the user could add too. An issue I ran into was that to use localStorage effectively you need to have a unique ID for each individual entry within localStorage. I ran into a problem and that’s what led me to make this function below. 

The issue was that when I would add multiple items into local storage and then delete them it would not delete the whole item. It would only delete small parts. I then looked into why this happens and saw that it would be best to use a unique ID that would be assigned to each item stored within localStorage. 

This is how I would set an item and also remove an item within localStorage.

![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641902822/ReadMe%20images/Project%202%20-%20Rapid%20Games/localstorageselect_mktrxm.png)

After looking into different ways I could have implemented this feature. I found that JavaScript has a built in object called Set which would let you store unique values of any type. This would have saved me a lot of time figuring out how to store unique values. I was happy that I did learn about this after, as it meant I could use this object in future projects.

E.g. 
Use to remove duplicate elements from the array

`const numbers = [2,3,4,4,2,3,3,4,4,5,5,6,6,7,5,32,3,4,5]
console.log([...new Set(numbers)])
[2, 3, 4, 5, 6, 7, 32])`

**My implementation:**
![alt text](https://res.cloudinary.com/dmpvulj3q/image/upload/v1641902820/ReadMe%20images/Project%202%20-%20Rapid%20Games/local_storage_function_ytwthn.png)

## Bugs

If you delete all your games from the myGame section the message “Create a collection of games doesn't show up”.
## Blockers

One of the main blockers in this project was the my games component, but after some persistence we got it to work in the end.

![alt text]()
## Wins

* Pair programming was a great experience.
* Using React to build a single page application. 
* Working with an API.
* Planning application features and then implementing them within the timeframe. 
* Using a CSS framework.

## Future features

Include pagination on homepage, browse games and search games components .

I wanted to include a feature that would count how many times the game was added to someone’s collection. I had done some digging online and came across countAPI (https://countapi.xyz). This API allows you to create simple numeric counters. IaaS, Integer as a Service.
## Key Learnings

Not over complicating the process, after writing code in a long winded way to get back only a unique Game ID. I did some more research after the project had finished and came to realise I could have used Set to handle this problem for me. 
