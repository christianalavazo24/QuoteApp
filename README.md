Android App Behavior:
1.	First Page (Main Screen):
o	Emotion Selection: Users will see a list of emotions (Scared, Sad, Tired, Anxious) displayed in a RecyclerView. They can select one emotion from this list.
o	Category Selection: Below the emotions, users will see a list of categories (Finance, Education, Relationship, Work, Friendship, Family) also displayed in a RecyclerView. Users can select one category.
2.	Submit Button:
o	After selecting an emotion and a category, the user clicks the Submit button.
3.	Notification Generation:
o	Upon clicking the Submit button, the app sends a request to the Laravel backend to fetch a random quote based on the selected emotion and category.
o	Once the backend returns a quote, the app displays a notification on the user's phone containing the following:
	Title: The author of the quote.
	Message: The quote itself.
Example Scenario Output:
•	If the user selects the emotion "Sad" and the category "Relationship" and clicks the Submit button, the app might generate a notification like:
o	Notification Title: Author1
o	Notification Text: "Quote 1"
(assuming that "Quote 1" corresponds to the selected emotion and category in the database.)
Backend Behavior (Laravel API):
1.	Quote Fetching:
o	When the user submits their selections, the Laravel API endpoint http://localhost:8000/api/quotes?emotion=Sad&category=Relationship is triggered.
o	The API looks up a random quote matching the selected Sad emotion and Relationship category in the quotes table.
o	It returns the quote in JSON format to the Android app.
Notification View:
•	After receiving the notification, the user can expand the notification to view the full quote and its author.

