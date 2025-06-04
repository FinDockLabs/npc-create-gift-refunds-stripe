<a href="https://githubsfdeploy.herokuapp.com?owner=FinDockLabs&repo=npc-create-gift-refunds-stripe&ref=main">
  <img alt="Deploy to Salesforce"
       src="https://raw.githubusercontent.com/afawcett/githubsfdeploy/master/deploy.png">
</a>

# Create Gift Refund records with FinDock for Fundraising & Stripe

The components in this repository extend how refunds are handled in the Salesforce Nonprofit Cloud data model from the Stripe dashboard. Instead of simply updating the Status on the Gift Transaction to "Fully Refunded," refunds processed through the Stripe dashboard will create a Gift Refund record to be attached to the Gift Transaction, which will reflect the appropriate values in the standard CurrentAmount and RefundedAmount fields.

## Requirements

The prerequisites to deploy this repository are:

- Fundraising enabled and configured in your Salesforce environment
- The FinDock for Fundraising package is installed
- The Stripe for FinDock package is installed

## Full list of components

Custom Tab
- Guided Matching Setups

Custom Fields
- cpm__Inbound_Report__c.Gift_Transaction__c
- cpm__Inbound_Report__c.Gift_Refund__c
- cpm__Inbound_Report__c.Created_Date_Date_Only__c

## Installation
1. Ensure your User has permissions to all objects referenced by the components in this repository. This includes FinDock permissions and Fundraising permissions.

2. Press the "Deploy to Salesforce" button at the top of this README and then press "Login to Salesforce" in the top right of your screen. Please note, the GitHub Salesforce Deploy Tool is provided open source by andyinthecloud. No FinDock support is provided.

3. Once installed, navigate to the "Guided Matching Setups" Tab where you will find a List View of all of the Guided Matching Rulesets (be careful not to select the "Guided Matching Setup" Tab which is the visual representation of the ruleset builder)

4. Find the record with the name "Inbound Report: PaymentHub-Stripe/charge.refunded" ([see screenshare](https://screen.studio/share/Rgly8317))

5. Copy the text from [HERE](/JSONChargeRefunded) and paste into the Rules field. Populate the Target field with "-".

6. Test by putting through a small payment and refunding through the Stripe dashboard. 

## Contributing

When contributing to this repository, please first discuss the change you wish to make via an issue or any other method with FinDock before making a change.

## Support

FinDock Labs is a non-supported group in FinDock that releases applications. Despite the name, assistance for any of these applications is not provided by FinDock Support because they are not officially supported features. For a list of these apps, visit the FinDock Labs account on Github. 

## License

This project is licensed under the MIT License - see the [LICENSE](/LICENSE) file for details
