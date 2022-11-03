# Social Networking Application (Beta App) Using Python

*This project is created with the collabortion of two of my colleagues.*

In this project we have created a GUI based social networking application (which we named it Beta) that manages posts and the social media accounts. Below are the requirements for implementing the project:

## Requirements:
1. Manage users, posts, followers, and newsfeed classes.
2. Create text files that contain information about these classes.
3. Users are of is two types: Individual and Business users
4. Users can follow other users in the system
5. User profile contains basic information: Profile photo, name, short biography, location, and birthdate.
6. Individual users can post their information in their dashboard.
7. A post can be live, picture, video, or text.
8. Followers can like or dislike the post
9. Business users can add additional information to their profile, such as website link. 10. Business users can also create advertisements
11. Business users can advertise their products to users’ newsfeed based on their payment plan.
* Basic plan: 10AED sends to 5 users
* Silver plan: 30AED send to 10 users
* Golden plan: 40AED send to 15 users
12. Newsfeed for a user only displays current week’s posts of the users he/she follows.
13. User’s newsfeed notifies the birthdays within a week.
14. Display newsfeed for a user on that date.
15. Display the users that received the advertisements from the business.

## Associated Classes with attributes and functions
| Class names   |Attributes |  Behaviors |
|---------------|------------|------------|
|Manager | -users: User[] <br> -posts: Posts[] <br>-UserFilename:string <br>-postsFilename:string | +readUsers() <br> +readPosts()|
|User | + name:string +password: <br> str +email:str <br> + followers:User [] <br> +posts: Posts [] | +setname(string) <br> +getstring(): string<br> +setpassword(strring) <br> +getpassword(): string <br> +getNewsfeed(Newsfeed()) <br> +setemail(string) <br> +getemail(): string <br> +setposts[Post] <br> +getposts(): Post <br> +setfollowers[User] <br> +getfollowers(): User|
|Individual |+maritalstatus: (single, married, divorced) | +setmaritalstatus(boolean) <br> +getmaritalstatus():boolean|
|Business |+websitelink: string <br> +paymentPlan: (Basic plan, Silver plan, Golden plan) | +setwebsitelink(string) <br> +getwebsitelink(): string <br> +setpaymentplan(string) <br> +getpaymentplan(): string|
|Profile |+profile_photo: png <br> +username: string <br> +birthdate: DATETIME <br> +location: string <br> + biography: string | +setprofilephoto(png) <br> +getprofilephoto(): <br> png +setusername(string) <br> +getusername(): string <br> +setbirthdate(DATETIME) <br> +getbirthdate(): DATETIME <br> +setlocation(string) <br> +getloaction(): string <br> +setbiography(string) <br> +getbiography(): string|
|Newsfeed |+ newsfeed= Posts{} + adsfeed= Ads{}| + post_hash: (Username:content) <br> +post_ad: (Business_name: content)|
|Post |+Username: User(name) <br> +content: (live, picture, video or text) <br> +like_num: int| +setusername(User) <br> +getterusername():User() <br> +setcontent(string) <br> +getcontent(): string <br> +setlike_num(int) <br> +getlike_num(): int |
|Ads |+Business_name:User(name)<br> +content: [live,picture,video or text] <br> +ad_link: string <br> + posts: Business(paymentPlan)| +setbusinessname(User) <br> +getbusinessname(): User() <br> +setcontent(string) <br> +getcontenxt(): string <br> +setad_link(string) <br> +getad_link(): string|

## Limitations 
The individual and business classes could not be displayed in a graphical user interface. We were unable to do so for the advertisements as well. Moreover, we could not create the birthday notification and weekly updated posts. 

## Files used
* User.py : user classes 
* Registration.py : register interface that saves the data to txt file 
* User gui.py : the interface of user's newsfeed and account profile, enable the user to like posts and create a post either pic or text
* Posts.txt : saving file for posts created by user 
* User.txt : saving file for users registered in the app 
