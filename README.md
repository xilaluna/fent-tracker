# Fentanyl Epidemic Tracker

[![Go Report Card](https://goreportcard.com/badge/github.com/xilaluna/Fentanyl-Epidemic-Tracker)](https://goreportcard.com/report/github.com/xilaluna/Fentanyl-Epidemic-Tracker)

The mission for this project was to create a scraper that would pull articles pertaining to fentanyl, for the goal of mapping the trend of the fentanyl epidemic & the increase of fentanyl distrubtion through illegal sites.

![graph image](/assets/graph.png)

## How it Works

1. How it works is quite simple, there is a simple go scraper built using colly which visits https://darknetlive.com/post/ and its next pages. The scraper then looks into each article and searches all the paragraphs for the word "fentanyl", if the article includes the word it will save the article name and the date it was published.
2. After the data is pulled it is then put into a json file where chart.js is able to display the amount of articles per month.

![scraper image](/assets/scraper-terminal.png)

## Tech Stack

- [Go](https://go.dev/)
- [Colly](http://go-colly.org/)
- [net/http](https://golang.org/pkg/net/http/)
- [Chart.js](https://www.chartjs.org/)
- JSON
- HTML

## Future Plans

- Store data in a database such as Redis.
- Create display to show each individual article.
