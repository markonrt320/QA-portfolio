# Test cases 

## Test Case 1: Verify employee

- **Priority**: 
- **Preconditions**: 
  - The user is logged in with an HR account.

### Steps

| Step | Test Steps                                    | Test Data                       | Expected Results                                           |
|------|-----------------------------------------------|---------------------------------|------------------------------------------------------------|
| 1    | Click| / | Employee  |
| 2    | Click | / | The employee(s |
| 3    | Enter | Employee    | Employee’s  |

Test Case 1: Verify monthly subscription to benefit with enough budget.
Scenario: Subscribe to benefit with monthly subscription.
Preconditions:
The user is logged in with a Member account. 
User has more budget than the benefit’s price.
Steps

Step
Test Steps
Test Data
Expected Results
1
Click the benefit card that has monthly subscription f.e. ‘Kućne posete med. osoblja’.
/
Benefit modal should appear on the screen.
2
Scroll down and press the ‘Subscribe’ button.
/
Benefit modal should be closed and a green pop up should appear with a message ‘Successfully subscribed to benefit’. In the bottom of the subscribed benefit card should appear text ‘Active from 01. Next month’.
Total budget should be decreased by the subscribed benefits value.
3
Click on the subscribed benefit card.
/
Button should have text ‘Subscribed’
4
Close the benefit card.
/
Benefit modal should be closed.
5
Scroll to the top and click on the budget button.
/
Total budget should be reduced by the amount of the subscribed benefit and in the section ‘Subscribed monthly’ should be increased by the same amount.
6
Click on ‘My Benefits’ button
/
Subscribed benefit should appear in ‘Next month’ section.



Test Case 2: Verify monthly subscription to benefit with not enough budget.
Scenario: Subscribe to benefit with monthly subscription.
Preconditions:
The user is logged in with a Member account. 
User has more budget than the benefit’s price.
Steps

Step
Test Steps
Test Data
Expected Results
1
Click the benefit card that has monthly subscription f.e. ‘Kućne posete med. osoblja’.
/
Benefit modal should appear on the screen. Subscribe button should be disabled.



Test Case 3: Verify one-time subscription to benefit with enough budget.
Scenario: Subscribe to benefit with one-time subscription.
Preconditions:
The user is logged in with a Member account. 
User has more budget than the benefit’s price.
Steps

Step
Test Steps
Test Data
Expected Results
1
Click the benefit card that has one-time subscription f.e. ‘Pregled stomatologa’.
/
Benefit modal should appear on the screen.
2
Scroll down and press the ‘Subscribe’ button.
/
Benefit modal should be closed and a green pop up should appear with a message ‘Successfully subscribed to benefit’. In the bottom of the subscribed benefit card should appear text ‘Active from 01. Next month’.
Total budget should be decreased by the subscribed benefits value.
3
Click on the subscribed benefit card.
/
Button should have text ‘Subscribed’
4
Close the benefit card.
/
Benefit modal should be closed.
5
Scroll to the top and click on the budget button.
/
Total budget should be reduced by the amount of the subscribed benefit and in the section ‘Subscribed one-time’ should be increased by the same amount.
6
Click on ‘My Benefits’ button
/
Subscribed benefit should appear in ‘Next month’ section.



Test Case 4: Verify one-time subscription to benefit with not enough budget.
Scenario: Subscribe to benefit with one-time subscription.
Preconditions:
The user is logged in with a Member account. 
User has less budget than the benefit’s price.
Steps

Step
Test Steps
Test Data
Expected Results
1
Click the benefit card that has one-time subscription f.e. ‘Video konsultacije sa lekarom’.
/
Benefit modal should appear on the screen. Subscribe button should be disabled.


Test Case 5: Verify voucher subscription to benefit with enough budget.
Scenario: Subscribe to benefit with voucher subscription.
Preconditions:
The user is logged in with a Member account. 
User has more budget than the benefit’s price.
Steps

Step
Test Steps
Test Data
Expected Results
1
Click the benefit card that has voucher subscription f.e. ‘Tickets’.
/
Benefit modal should appear on the screen.
2
Scroll down and press ‘Vaučer… text’
/
Dropdown should appear.
3
In dropdown select ‘Vaučer 6.000’ and press ‘Redeem’.


Benefit modal should be closed and a green pop up should appear with a message ‘Successfully subscribed to benefit’. In the bottom of the subscribed benefit card should appear text ‘Active from 01. Next month’.
Total budget should be decreased by the subscribed benefits value.
4
Click on the subscribed benefit card.
/
Button should have text ‘Redeemed’
5
Close the benefit card.
/
Benefit modal should be closed.
6
Scroll to the top and click on the budget button.
/
Total budget should be reduced by the amount of the subscribed benefit and in the section ‘Subscribed vouchers’ should be increased by the same amount.
7
Click on ‘My Benefits’ button
/
Subscribed benefit should appear in ‘Next month’ section.



Test Case 6: Verify voucher subscription to benefit with not enough budget.
Scenario: Subscribe to benefit with voucher subscription.
Preconditions:
The user is logged in with a Member account. 
User has less budget than the benefit’s price.
Steps

Step
Test Steps
Test Data
Expected Results
1
Click the benefit card that has voucher subscription f.e. ‘Tickets’.
/
Benefit modal should appear on the screen. 
2
Scroll down and press ‘Vaučer… text’
/
Dropdown should appear.
3
In dropdown select ‘Vaučer 6.000’.


Redeem button should be disabled.




Test Case 7: Verify vouchers subscription using lower boundary of vouchers value.
Scenario: Subscribe to benefit with voucher subscription.
Preconditions:
The user is logged in with a Member account. 
User has more budget than the benefit’s price.
Steps

Step
Test Steps
Test Data
Expected Results
1
Click the benefit card that has monthly subscription f.e. ‘Dexyco, poklon vaučer kartice’.
/
Benefit modal should appear on the screen.
2
Scroll down to ‘Školski vaučer’ and fill input field.
999
Message should appear ‘Minimum voucher price is 1000RSD’ and ‘Redeem’ button should be disabled.
Total budget should remain the same.



Test Case 8: Verify vouchers subscription using boundary of vouchers value.
Scenario: Subscribe to benefit with voucher subscription.
Preconditions:
The user is logged in with a Member account. 
User has more budget than the benefit’s price.
Steps

Step
Test Steps
Test Data
Expected Results
1
Click the benefit card that has monthly subscription f.e. ‘Dexyco, poklon vaučer kartice’.
/
Benefit modal should appear on the screen.
2
Scroll down to ‘Školski vaučer’ and fill input field.
1000
‘Redeem’ button should be enabled.
3
Click ‘Redeem’ button.
/
Benefit modal should be closed and a green pop up should appear with a message ‘Successfully subscribed to benefit’. In the bottom of the subscribed benefit card should appear text ‘Active from 01. Next month’.
Total budget should be decreased by the subscribed benefits value.



Test Case 9: Verify vouchers subscription using upper boundary of vouchers value.
Scenario: Subscribe to benefit with voucher subscription.
Preconditions:
The user is logged in with a Member account. 
User has more budget than the benefit’s price.
Steps

Step
Test Steps
Test Data
Expected Results
1
Click the benefit card that has monthly subscription f.e. ‘Dexyco, poklon vaučer kartice’.
/
Benefit modal should appear on the screen.
2
Scroll down to ‘Školski vaučer’ and fill input field.
1001
‘Redeem’ button should be enabled.
3
Click ‘Redeem’ button.
/
Benefit modal should be closed and a green pop up should appear with a message ‘Successfully subscribed to benefit’. In the bottom of the subscribed benefit card should appear text ‘Active from 01. Next month’.
Total budget should be decreased by the subscribed benefits value.


Test Case 10: Verify vouchers subscription to benefit with not enough budget.
Scenario: Subscribe to benefit with voucher subscription.
Preconditions:
The user is logged in with a Member account. 
User has more budget than the benefit’s price.
Steps

Step
Test Steps
Test Data
Expected Results
1
Click the benefit card that has monthly subscription f.e. ‘Dexyco, poklon vaučer kartice’.
/
Benefit modal should appear on the screen.
2
Scroll down to ‘Školski vaučer’ and fill input field.
22
‘Redeem’ button should be enabled.
3
Click ‘Redeem’ button.
/
Benefit modal should be closed and a green pop up should appear with a message ‘Successfully subscribed to benefit’. In the bottom of the subscribed benefit card should appear text ‘Active from 01. Next month’.
Total budget should be decreased by the subscribed benefits value.




Test Case 11: Verify subscription using upper boundary value.
Scenario: Subscribe to benefit with voucher subscription.
Preconditions:
The user is logged in with a Member account. 
User has more budget than the benefit’s price.
Steps

Step
Test Steps
Test Data
Expected Results
1
Click the benefit card that has monthly subscription f.e. ‘Dexyco, poklon vaučer kartice’.
/
Benefit modal should appear on the screen.
2
Scroll down to ‘Školski vaučer’ and fill input field between - and +.
45
Message should appear ‘You don’t have enough tokens to subscribe.’ and ‘Redeem’ button should be disabled.
Total budget should remain the same.




Test Case 12: Verify subscription using available boundary of stock value.
Scenario: Subscribe to benefit that has stock.
Preconditions:
The user is logged in with a Member account. 
User has more budget than the benefit’s price.
Steps

Step
Test Steps
Test Data
Expected Results
1
Click the benefit card ‘Dostava voća i povrća’.
/
Benefit modal should appear on the screen.
2
Scroll down to ‘Mesecni paket - mini’ and fill input field.
19
‘Subscribe’ button should be enabled.
3
Click ‘Subscribe button.
/
Benefit modal should be closed and a green pop up should appear with a message ‘Successfully subscribed to benefit’. In the bottom of the subscribed benefit card should appear text ‘Active from 01. Next month’.
Total budget should be decreased by the subscribed benefits value.



Test Case 13: Verify subscription using boundary of stock value.
Scenario: Subscribe to benefit that has stock.
Preconditions:
The user is logged in with a Member account. 
User has more budget than the benefit’s price.
Steps

Step
Test Steps
Test Data
Expected Results
1
Click the benefit card ‘Dostava voća i povrća’.
/
Benefit modal should appear on the screen.
2
Scroll down to ‘Mesecni paket - mini’ and fill input field.
20
‘Subscribe’ button should be enabled.
3
Click ‘Subscribe button.
/
Benefit modal should be closed and a green pop up should appear with a message ‘Successfully subscribed to benefit’. In the bottom of the subscribed benefit card should appear text ‘Active from 01. Next month’.
Total budget should be decreased by the subscribed benefits value.



Test Case 14: Verify subscription using unavailable boundary of stock value.
Scenario: Subscribe to benefit that has stock.
Preconditions:
The user is logged in with a Member account. 
User has more budget than the benefit’s price.
Steps

Step
Test Steps
Test Data
Expected Results
1
Click the benefit card ‘Dostava voća i povrća’.
/
Benefit modal should appear on the screen.
2
Scroll down to ‘Mesecni paket - mini’ and fill input field.
21
‘Subscribe’ button should be enabled.
3
Click ‘Subscribe button.
/
Benefit modal should stay opened and a red pop up should appear with a message ‘Not enough items available’.
Total budget should remain the same.



Test Case 15: Verify unsubscription from benefit from modal.
Scenario: Unsubscribe from benefit.
Preconditions:
The user is logged in with a Member account. 
User is subscribed on benefit.
Steps

Step
Test Steps
Test Data
Expected Results
1
Scroll to subscribed benefit and open it.
/
Benefit modal should appear on the screen.
2
Scroll to button ‘Unsubscribe’ and click it.
/
Benefit modal should be closed and a green pop up should appear with a message ‘Successfully unsubscribed from benefit’. 
Total budget should increase by the unsubscribed benefits value.
3
Scroll to the top and click ‘My benefits’ button.
/
In section ‘Next month’ should not contain benefit that user unsubscribed from. 


Test Case 16: Verify unsubscription from benefit from ‘My Benefits’ section.
Scenario: Subscribe to benefit that has stock.
Preconditions:
The user is logged in with a Member account. 
User is subscribed on benefit.
Steps

Step
Test Steps
Test Data
Expected Results
1
Click ‘My Benefits’.
/
All subscribed benefits should appear on the page.
2
Click on any subscribed benefit.
/
Benefit modal should appear on the screen.
3
Scroll to the subscribed section and click on ‘Subscribed’ button.
/
Benefit modal should be closed and a green pop up should appear with a message ‘Successfully unsubscribed from benefit’. 
In section ‘Next month’ should not contain benefit that user unsubscribed from.
Total budget should increase by the unsubscribed benefits value.



Test Case 17: Add benefit to favorite by clicking heart img.
Scenario: Add to favorite.
Preconditions:
The user is logged in with a Member account.
Steps

Step
Test Steps
Test Data
Expected Results
1
Click on heart image on the bottom right corner of Benefits card.
/
Heart should be whole red. Benefit modal should be closed and a green pop up should appear with a message ‘Successfully added Benefit to favorites’. 


2
Scroll to top and click ‘Favorite Benefits’.
/
Previously Benefit that was set as favorite should appear with all other benefits that was set as favorite.



Test Case 18: Add benefit to favorite from modal.
