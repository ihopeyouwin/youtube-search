# youtube-search  
</br>
https://ihopeyouwin.github.io/youtube-search/index.html -  view
</br>
put a search phrase into a search-field  </br>
click on a video to open up a player  </br>
click to the left or the right of the side of the player to close it  </br>
hold on the mouse under the video list and drag to the left to switch pages  </br>
</br>
</br>
</br>
</br>
</br>
</br>

# YouTube client

### Task:
The task is to create a web app to view the information about youtube clips on user request.
YouTube REST API should be accessed via cross-domain XHR requests.

### Use case:
1. User sees a search box as he starts up the app.
2. The user inputs a request in the search box. e.g. - javascript  
3. The app processes the request to YouTube REST API and displays loaded clips as a horizontal list of items.
4. The horizontal list can be scrolled with a swipe (on a desktop via mouse swipe). Swipe should be animated, e.g. user can click and pull the list sideways. Paging event should be triggered when mouseUp is released. If a user makes X quick swipes the app should list X pages. The number of clips on the page depends on its size (1 to 4 clips per page).      
5. The additional navigation buttons (paging control) are set at the bottom of the page.  
6. As the app lists the pages it should load new data in chunks ( 15 clips per chunk). It would be good to manage "smooth" data loading which means preloading data chunks in advance to emulate infinite scrolling experience.

### Requirements
1. Perfect for latest Chrome;
2. Support at least one mobile browser(e.g. iOS / Android / WP);
3. Clips (aka components) are listed pagely. Resizing the page increases/decreases the number of clips on a page. After a resize event the first left clip from the previous state should be present in the new state (but its position can be different). The further resizing would take into the account the first left component from the new state.
4. During a mousedown event on a paging component the tooltip with page number should pop-up.
5. Your complete app should be uploaded to github pages (gh-pages branch) or to any other hosting.
6. Each clip-component should provide the following information about a single YouTube clip:
    - title (includes a clickable link to YouTube)
    - clip preview as a picture
    - video description
    - author (channel name)
    - upload date
    - view count

    Showing any other information is optional.
    
### Samples of YouTube REST API requests:
    - https://www.googleapis.com/youtube/v3/search?key=AIzaSyCTWC75i70moJLzyNh3tt4jzCljZcRkU8Y&type=video&part=snippet&maxResults=15&q=js
    - https://www.googleapis.com/youtube/v3/videos?key=AIzaSyCTWC75i70moJLzyNh3tt4jzCljZcRkU8Y&id=nq4aU9gmZQk,REu2BcnlD34,qbPTdW7KgOg&part=snippet,statistics
    - How to get an API key - https://www.youtube.com/watch?v=JbWnRhHfTDA
    - You can find a more detailed documenation here - https://developers.google.com/youtube/v3/

### UI Examples:
#### Default view:
![](https://i.imgur.com/W7CTv9X.png)

#### Resized window
![](https://i.imgur.com/U5QX7cA.png)

#### Mobile version
![](https://i.imgur.com/MIFv1sV.png)
    
## Source code requirements 
- HTML rendering via JavaScript (a page is loaded without html tags inside document.body);
- CSS preprocessors can be used; 
- CSS3 Animations with Transitions & Transforms;
- Use of jQuery and other frameworks and libs **is forbidden** (except for https://lodash.com/);
- `.editorconfig` is required
- `eslint` is required
- `eslint-config-airbnb-base` is required
-  JS code should be split into modules and assembled by Webpack. Usage of babel and babel-loader is required. 
