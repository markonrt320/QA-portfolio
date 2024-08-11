# Test cases 

## Test Case 1: Verify 'Reset All Filters' Button After Partial Filter Application.

- **Scenario**: Reset all filters.
- **Preconditions**: 
  - The user is logged in with a Member account.

### Steps

| Step | Test Steps                                    | Test Data                       | Expected Results                                           |
|------|-----------------------------------------------|---------------------------------|------------------------------------------------------------|
| 1    | Apply sorting by benefit groups. | 200-400 | Results are sorted according to the selected benefit group.  |
| 2    | Select a benefit type from the benefit type filter. | voucher | The results are filtered to show benefits related to the selected benefit type.s |
| 3    | Select a category from the category filter. |  home | The results are filtered to show benefits related to the selected category.  |
| 4    | Click the "Reset All Filters" button. |  /| All applied filters (sorting, benefit type, and category) are cleared. Results are restored to the default state, showing all available benefits without any specific filtering.  |


## Test Case 2: Filter benefits value in the range of 300-400.

- **Scenario**: Filter benefits by value.
- **Preconditions**: 
  - The user is logged in with a Member account.

### Steps

| Step | Test Steps                                    | Test Data                       | Expected Results                                           |
|------|-----------------------------------------------|---------------------------------|------------------------------------------------------------|
| 1    | Enter the value in the left input box of the price filter. | 300 | The benefits section should display only benefits with values greater than or equal to 300.  |
| 2    | Enter the value in the right input box of the price filter. |400 | The benefits section should display only benefits with values less than or equal to 400. |


## Test Case 3: Remove benefit from favorite from benefit modal.

- **Scenario**: Remove from favorite.
- **Preconditions**: 
  - The user is logged in with a Member account.
  - User has set benefit to favorite.

### Steps

| Step | Test Steps                                    | Test Data                       | Expected Results                                           |
|------|-----------------------------------------------|---------------------------------|------------------------------------------------------------|
| 1    | Scroll to the benefit that was set to favorite and click on it. | / | Benefit modal should appear on the screen.  |
| 2    | Click on ‘Remove from favorites’ button. | / | Button should have text ‘Add to Favorites’. Modal should remain open and a green pop up should appear with a message ‘Successfully removed benefit from favorites’.  |
| 3    | Scroll to the top of the modal and click X. | / | Benefit modal should be closed.  |
| 4    | Scroll to top and click ‘Favorite Benefits’. | / | Benefit that was unset from favorite should not appear in Favorite benefits section.  |

## Test Case 4: Verify voucher subscription to benefit with not enough budget.

- **Scenario**: Subscribe to benefit with voucher subscription.
- **Preconditions**: 
  - The user is logged in with a Member account.
  - User has less budget than the benefit’s value.

### Steps

| Step | Test Steps                                    | Test Data                       | Expected Results                                           |
|------|-----------------------------------------------|---------------------------------|------------------------------------------------------------|
| 1    | Click the benefit card that has voucher subscription f.e. ‘Tickets’. | / | Benefit modal should appear on the screen. |
| 2    | Scroll down and press ‘Vaučer’ text | / | Dropdown should appear. |
| 3    | In dropdown select ‘Vaučer 6.000’. | / | Redeem button should be disabled.  |


## Test Case 5: Verify monthly subscription to benefit with enough budget.

- **Scenario**: Subscribe to benefit with monthly subscription.
- **Preconditions**: 
  - The user is logged in with a Member account.
  - User has more budget than the benefit’s value.

### Steps

| Step | Test Steps                                    | Test Data                       | Expected Results                                           |
|------|-----------------------------------------------|---------------------------------|------------------------------------------------------------|
| 1    | Click the benefit card that has monthly subscription f.e. ‘Kućne posete med. osoblja’. | / | Benefit modal should appear on the screen. |
| 2    | Scroll down and press the ‘Subscribe’ button. | / | Benefit modal should be closed and a green pop up should appear with a message ‘Successfully subscribed to benefit’. In the bottom of the subscribed benefit card should appear text ‘Active from 01. Next month’. Total budget should be decreased by the subscribed benefits value. |
| 3    | Click on the subscribed benefit card. | / | Button should have text ‘Subscribed’.  |
| 4    | Close the benefit card. | / | Benefit modal should be closed.  |
| 5    | Scroll to the top and click on the budget button. | / | Total budget should be reduced by the amount of the subscribed benefit and in the section ‘Subscribed monthly’ should be increased by the same amount.  |
| 6    | Click on ‘My Benefits’ button. | / | Subscribed benefit should appear in ‘Next month’ section.  |


### Other test cases can be found [here](https://docs.google.com/document/d/1WtYlnkMlRStEb4Dfh6BqkTbG6ZnPdvr-XqLfFeulIF0/edit?usp=sharing)
