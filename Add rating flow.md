#### Step 1:

Function **controlAddRatingFlow** will be called first from index.php to controller which is used to show the payout done confirm form.

- First we get the user id by calling function **getUserID**.
- Function **showAddRating** takes the input data object and gives to show the meeting rating form.
- In action, function **showAddRating** will be called from MeetingView.php which displays the rating form tpl page.
- The display tpl page will be **addRating.tpl** in views folder.
