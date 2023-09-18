# FidelityHelper
Tired of manually calculating how much tax you'll have to pay when you sell shares from Fidelity ? 
This chrome extension will help you get an overview before withdrawing a said amount.

### Why do we need this? 

- Fidelity website is built keeping in mind US Customers as has no taxation visibility for Indian customers. 
- Before selling some number of stocks, it is very tedious for a customer to calculate the tax which he/she will have to pay for the redeemed amount. 
This extension will give the user an estimate of how much tax he/she will have to pay if they redeem a certain amount of stock keeping in mind the current tax laws in India and the customer’s slab rate. 

### How to use?
- Clone this repo.
- Open Google Chrome browser and go to `Settings` -> `Extensions`.
- Enable developer mode and click on "Load Unpacked" option. Select the folder where you cloned the repo previously. More info [here.](https://support.google.com/chrome/a/answer/2714278?hl=en#:~:text=Go%20to%20chrome%3A%2F%2Fextensions,the%20app%20or%20extension%20folder.)
- Login to your Fidelity Netbeneifts account. From the homepage click on "View Share Details" option.
- Once the Share details page loads, Open the Fidelity Helper chrome extension and enter your tax slab rate and the number of stocks you wish to withdraw.

  ![main page blurred](https://github.com/FidelityHelper/fidelityTaxhelper/assets/104997027/d9a792ef-ee98-4bf3-9db4-d061cffbc128)
- Click on Calculate button and you'll see that the extension will populate a new column in the table showing tax applicable if you sell on the current date for a particular entry.

  
![after calculate blurred](https://github.com/FidelityHelper/fidelityTaxhelper/assets/104997027/debc5538-9f2b-4906-84e2-a113cb933c65)
- Also, it will show cumulative tax according to the number of stocks you wish to sell.


### How does it work?
The extension picks up data from “View share details” modal in fidelity using content scripting and processing it to get the required data. For STCG (<24 months holding), the user is taxed at slab rate.  For LTCG (>=24 months holding), the user is taxed at 20% with indexation benefit. The data is then fed back to the page and displayed to the user.

### Privacy
This extension reads the fidelity webpage to only display the tax liability inline. No data is collected, stored, transfered or used in any other way.

### Contributing
We welcome contributions. Please make a detailed PR with your change and we will be happy to review.

### Disclaimer
> This extension does not take into account the USD to INR currency exchange rates on the date of purchase. This is why the tax liability data is not 100% accurate. It is advised to check with one's CA for an accurate measure of the tax liability for income tax purposes.
