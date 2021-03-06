## Final Project

The following is a sample project to put to practice all the topics learned so far. The definitions and functionalities are provided in a close to reality fashion.
You will be provided with a list of features that the sample applications must have, along with a set of wireframes to guide how the app should look like.
To accomplish the desired features, you will need to consume different services to get the data needed to populate the  views.

Use the latest version of Angular, following the app structure generated by the ng client.

#### Wireframes

##### Home

<p align="center">
  <img height="80%" width="80%" src="https://github.com/eabait/bootcamp-ui-2020/blob/master/final-project/wireframes/home.png">
</p>

##### Twitter Details

<p align="center">
  <img height="40%" width="40%" src="https://github.com/eabait/bootcamp-ui-2020/blob/master/final-project/wireframes/tweet_details.png">
</p>

##### Search & Trends

<p align="center">
  <img height="80%" width="80%" src="https://github.com/eabait/bootcamp-ui-2020/blob/master/final-project/wireframes/search_1.png">
</p>
<p align="center">
  <img height="80%" width="80%" src="https://github.com/eabait/bootcamp-ui-2020/blob/master/final-project/wireframes/search_2.png">
</p>

##### Configuration

<p align="center">
  <img height="40%" width="40%" src="https://github.com/eabait/bootcamp-ui-2020/blob/master/final-project/wireframes/configuration.png">
</p>


#### Stories

1. As a user, I want to see my twitter timeline.

2. As a user, I want to see a specific twitter details.

3. As a user, I want to see my country trends.

4. As a user, I want to search on twitter to quickly find news and events.

5. As a user, I want to see all the results for a specific search (with pagination).

6. As a user, I want to configure what I want to see in my twitter timeline. This configuration must be reflected in the home section.


#### Set Up Twitter Server

1. Open the console
2. Step inside `server` folder
3. Execute `npm install`
4. Execute the command `node server` in the console
5. Open the browser and type `localhost:8080`
6. You should see this text on the brower `Twitter API is running...`

#### Endpoints

#### GET statuses / home_timeline

endpoint: /timeline?count=100

Returns a collection of the most recent Tweets posted by the authenticating user and the users they follow.

##### Parameters

**count (optional)**: Specifies the number of records to retrieve. Must be less than or equal to 200. Defaults to 20. The value of count is best thought of as a limit to the number of tweets to return because suspended or deleted content is removed after the count has been applied.

#### GET trends/place

endpoint: /trends?id=23424747

Returns the top 50 trending topics for a specific WOEID, if trending information is available for it.

##### Parameters

**id (required)**: The Yahoo! Where On Earth ID of the location to return trending information for. Global information is available by using 1 as the WOEID .

#### GET search/tweets

endpoint: /search?q=TanBionicaCocaColaFM

Returns a collection of relevant Tweets matching a specified query.. This search API searches against a sampling of recent Tweets published in the past 7 days. Part of the 'public' set of APIs.

##### Parameters

**q (required)**: A UTF-8, URL-encoded search query of 500 characters maximum, including operators. Queries may additionally be limited by complexity.

#### GET statuses/show/:id

endpoint: show?id=1011417658833551361 (id_str)

Returns a single Tweet, specified by the id parameter. The Tweet’s author will also be embedded within the Tweet.

##### Parameters

**id** (required): The numerical ID of the desired Tweet.
