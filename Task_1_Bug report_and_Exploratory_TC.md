# Task 1 (Bug report and exploratory testcases - Monefy App [Android])

[Monefy](https://play.google.com/store/apps/details?id=com.monefy.app.lite) is a personal finance application that makes
money management easy. It is designed to streamline expense tracking and help user in saving money.

## Resources

* App version - 1.16.0
* Device - OnePlus 8 Pro
* Android version - 12

## Docket
- [Bugs Discovered](task.md#bugs-discovered)
- [Exploratory Charters](/task.md#exploratory-test-charters)
- [Charter Prioritization](task.md#charter-prioritization)
- [Risks](task.md#risks)



## Bugs Discovered

| App Feature                               | Steps to reproduce                                                                                                                                   | Actual Result                                                                                                              | Expected Result                                                                                                                                                                         |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dashboard                                 | On app first time launch tutor explains some feature about the app                                                                                   | Not much information about the app                                                                                         | Tutorial can be more detailed and explain some more feature                                                                                                                             |
| Dashboard                                 | Add expense under a category -> go to dashboard -> Icons position changes randomly                                                                   | Category icons position changes when an amount is entered in a category                                                    | Icons position should either be static or user can organize them                                                                                                                        |
| Dashboard                                 | On dashboard click on balance button -> swipe down to go back to dashboard                                                                           | No option to swipe down to dashboard, only clicking on hamburger icon will take back to dashboard                          | Swipe down from balance screen to dashboard should be there.                                                                                                                            |                                                                                   | 
| Dashboard -> Transfer                     | Select account type as  "All accounts" from top left under filter -> Make a transfer from cash to card -> Go to dashboard -> balance summary list    | Transfer done is not mentioned in the summary                                                                              | Transfers should be shown even under "all accounts" mode.                                                                                                                               | 
| Dashboard -> Search                       | Click on search icon -> Enter category + amount in search text box -> Example we have a expense of 100.00 under clothes section -> Enter 'Clothes 1' | Search filter does not show the expense of Clothes 100.00 if complete amount is not entered                                | Search on regex should also be supported like 'Clothes 1' should show 'Clothes 100.00' as well.In case user wants to search only for 'Clothes 1' maybe add option to enclose in quotes. |
| Dashboard -> Update transaction           | On balance summary select any transaction -> On edit screen update the amount to any value -> Press back                                             | Amount is updated to the new value                                                                                         | On pressing back message should be displayed regarding changes will be lost and not auto save the updates                                                                               |
| Dashboard -> Balance Summary              | Select account type as  "All accounts" from top left under filter -> Go to balance summary list on dashboard                                         | No icon or text to idetify the account type(cash/card) for each transaction                                                | Icon or label to associate transaction with account type like cash/card                                                                                                                 |
| Dashboard -> Add/Update Expense or Income | On add income/expense screen enter an amount -> press + -> press =                                                                                   | It adds original amount to itself                                                                                          | It should maybe take 0 as the second input in case any operation (+-/*) is performed on a number without second number input                                                            |
| Dashboard -> Add/Update Expense or Income | On add income/expense screen enter an amount -> To update the very first digit of amount user has to delete all the digits                           | Not possible to edit a particular digit without deleting all the number after it                                           | User can place the cursor on particular digits                                                                                                                                          | 
| Dashboard -> Add/Update Expense or Income | On add income/expense screen -> Select date on top                                                                                                   | In order to select date from past year user has to swipe through each month, no option to select month & date              | There should be option to select month and year as well                                                                                                                                 | 
| Seetings -> Language                      | On settings tab -> select language as espanol                                                                                                        | Not all text and labels have changed to espanol, rather they are in english only (like the filter has text like Day, Week) | All the text and labels should be translated to changed language                                                                                                                        |
| Right side tab -> Accounts                | Select all the account and delete each one of them                                                                                                   | All the accounts are deleted successfully                                                                                  | Disable deleting account if there is only one account left or add a warning message that this is the last account configured                                                            |
| Right side tab -> Accounts                | Add new account with the name 'Cash' -> Add another account with same name 'Cash'                                                                    | Account is created successfully                                                                                            | Error on creation of account with same name .It can be confusing to have two accounts under same name                                                                                   |                                                                                   |
| Settings                                  | Go to settings -> Change the 'First day of Week' -> Go back to dashboard                                                                             | No change on dashboard. Reset to some other date filter and then back to week will show the changes                        | Dashboard should be refreshed with new week first day of week as soon as settings are changed.                                                                                          |                                                                                   |
| Settings                                  | Go to settings -> Change the 'First day of Month' -> Go back to dashboard                                                                            | No change on dashboard. Reset to some other date filter and then back to month will show the changes                       | Dashboard should be refreshed with new week first day of month as soon as settings are changed.                                                                                         |                                                                                   |
| Settings                                  | Go to settings -> Enable budget mode -> Enter any amount                                                                                             | Budget will be displayed with blue color on dashboard center  but income is hidden                                         | Income should also be displayed in center screen when budget is enabled                                                                                                                 |                                                                                   |
| Dashbaord                                 | No option on dashboard to filter sum of expense for certain categories                                                                               | -                                                                                                                          | Option to filter out certain categories and see the total expense only specific to these categories                                                                                     |                                                                                   |


## Exploratory Test Charters

✅ - Results are as expected

❗ - Area of improvement from UX perspective

> Note - Test cases with bugs are mentioned under bugs section with more description.

| Charter 01 | To install, uninstall & launch the app |
| -----------| -------------------------------------- |
| Notes      | Install the app from play store ✅<br> Launch the app after installation and verify it launches smoothly without crashing ✅ <br> Force kill the app, verify if it re-launches successfully ✅<br> Keep the app running in background and verify if it doesn't crashes automatically ✅<br/> |

| Charter 02 | Explore the Dashbaord & Income/Expense Management |
| -----------| -------------------------------------- |
| Notes      |Tour guide to the dashboard is displayed on first time dashbaord launch [Could have been more informative] ❗ <br> Add new income by clicking on "Income" icon ✅<br> Add amount with 2 decimal digits(cents/paisa) ✅ <br> Select account type, defaults to Cash if nothing is selected ✅<br> Select income category from default options as "Deposit/Salary/Savings" ✅ <br> Option to create new income category with multiple choices for icon ✅  <br> |

| Charter 03 | To explore the search feature          |
| -----------| -------------------------------------- |
| Notes      |  Enter category to serch all the income/expense under that categroy ✅<br> Enter amount to search all the expense/income entries matching the amount ✅<br> Search by category + amount details ✅<br> Edit expense/income by clicking on that entry in search result ✅<br> |

| Charter 04 | To explore the transfer feature        |
| -----------| -------------------------------------- |
| Notes      |  Add new transfer from one account type like 'Cash' to 'Payment Card' and vice versa ✅<br> Option to make transfer from/to user created account type ✅ <br>Doesn't allow transfer within same account type, like cash to cash ✅<br> |

| Charter 05 | To explore Filter -> Accounts |
| -----------| ---------------------------------------- |
| Notes      | Default value is "All accounts" along with currency ✅ <br> Click on accounts to show all the current accounts ✅ <br> By default there are 2 account types - "Cash" & "Payment Card" ✅ <br> Selecting a particular account displays all the expense/income on dashboard for that particular account ✅ <br> Select "All accounts" to get a cumulative income/expense result on dashboard ✅ |

| Charter 06 | To explore Filter -> Date Range |
| -----------| ---------------------------------------- |
| Notes      | Default date range selected is current day ✅ <br> Select date range to Week/Month/Year/All ✅ <br> Selecting a particular date range will traverse back to dashboard and filter out the transactions for the selected date range, with and without carryover✅ <br> |

| Charter 07 | To explore Right Side Tab -> Categories |
| -----------| ---------------------------------------- |                               
| Notes      | Option to add new category under the expense tab [Pro membership required] ✅ <br> Option to add new category under the income tab [pro membership required] ✅ <br> Change the icon for a income/expense category [pro membership required] ✅ <br> Change expense/income category name ✅ <br> |

| Charter 08 | To explore Right Side Tab -> Accounts |
|------------| ---------------------------------------- |
| Notes      | Default 2 values are there under account section "Cash" and "Payment Card" ✅ <br> Each account section shows the corresponding balance under the account name ✅ <br> Edit account name ✅ <br> Change account currency [Pro membership required] ✅ <br>|

| Charter 09 | To explore Right Side Tab -> Settings |
|------------| ---------------------------------------- |
| Notes      | Option to set 'Budget mode' which is disabled by default ✅ <br> To enable the budget mode add a amount > 0  and without decimals ✅ <br> Budget will be displayed in blue color in center of dashboard, and only when account type is "All accounts" ✅ <br> Option to carryover amount from previous week/month/year to next week/month/year, which is disabled by default ✅ <br> When carryover is enabled it will display the carryover amount in dark green on dashboard screen and as "Carry Over" in balance summary ✅ <br>|


## Charter Prioritization

| Priority | Charter &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;                                                  | Reason                                                                                                                                                                                                                                                                                                                                             |
|----------|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| P0       | Charter 01  <br> Charter 02                                | App launch and installation is priority, because any issues faced with installation, launch(app is not launching/taking time to launch) or frequent crashes may hamper user initial experience <br/> Charter 01 tests the core functionality of this app which is add/update/delete an income or expense and so it should be explored on priority. |
| P1       | Charter 09 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;                                               | In order to explore other features of the app user may need to change app language, currency or layout. This can be a blocker for some users(change default language) in case there are issues with setting functionality .                                                                                                                        |
| P2       | Charter 03 <br> Charter 06                                | To filter and search for records smoothly. Any issues with this feature may not be a blocker and hence not a P0/P1.                                                                                                                                                                                                                                |
| P3       | Charter 04 <br> Charter 07 <br> Charter 08 <br>Charter 05 | Additional features provided by the app                                                                                                                                                                                                                                                                                                            |


## Risks

* Limitation to test pro versions features like currency, synchronization and theme options which required membership.
* In case a user subscribes to pro membership and cancels it, there should be no charge on user card in the future.
* App performance can be tested on device with less RAM and restricted hardware configuration.
* If a user subscribes to pro version and switches device subscription should be redeemed on the new device as well. 
* Limitation to check on how many devices a subscription can run in parallel for same user.
* This testing was done only a specific brand of android phone, limitation of android/ios devices can make it hard to test app on different size of devices and os versions.