# Subscription UI

In your project, you can use the Subscription UI to manage your subscriptions card. Your subscription cards will be displayed in the Subscription Card section. You can use the Subscription UI to manage the look and feel for each of your subscription card.

### Subscription Card

The Subscription Card section displays all the subscription cards that you have created. You can create a new subscription card by adding a new Subscription Role to your project.

![Subscription Card](/img/ui/subscription-cards.png)

### Editing Subscription Card

It is important to note that the Subscription Card UI is only for managing the look and feel of the subscription card. To manage the subscription card content, you will need to use the Subscription Role UI to content like Subscription Name, Subscription Description, Subscription Price, etc.

In each subscription card, you need to make sure of the following:

- 1. Ensure you don't make changes to id values of different elements in the card.
     here is a table of all important ids that are required for the card to work properly.

| ID                       | Info                                                                                                        |
| ------------------------ | ----------------------------------------------------------------------------------------------------------- |
| plan-name-\*             | This is the id of the element that displays the subscription name.                                          |
| plan-image-\*            | This is the id of the element that displays the subscription image.                                         |
| subscription-price-\*    | This is the id of the element that displays the subscription price.                                         |
| subscription-type-\*     | This is the id of the element that displays the subscription type (e.g., monthly, yearly).                  |
| subscription-purchase-\* | This is the id of the button that allows users to purchase the subscription.                                |
| subscription-info-\*     | This is the id of the element that displays additional information or messages related to the subscription. |
| included-features-\*     | This is the id of the container that lists the features included in the subscription plan.                  |

- 2. Ensure you don't add any other values to the card that implies irregularities in the card information.

- 3. Ensure you don't remove any of the elements in the card.

to Learn more about how to enable Subscription or how to create a new subscription card, please refer to Monetization section in the [User Guide](/monetization/subscriptions).
