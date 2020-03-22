# bailout.nyc

When we began working on this project to help provide financial relief to service workers, one of our **KEY REQUIREMENTS** was to build something *QUICKLY*.

Below is a rough description of how we built bailout.nyc. Please feel free to clone this project to create your own version to support your local community.

## 1. Fork this repo on github

Pretty much everything is in `index.html` with some key configuration at the top.

## 2. Create a registration form on Google Forms

Ours asks for:

- Business Name
- Physical Business Address
- Description of where the funds will go and why they're needed
- What are 5 adjectives that describe your staff?
- What's keeping you hopeful through this time?
- Venmo Username (e.g. @JoePizzaHelpStaff)
- GoFundMe Link
- Verify that it's you by DM-ing your Venmo username to @bailoutnyc on Instagram or Twitter from your business account, or by posting publicly about bailout.nyc.

Get the **Share URL** for the form by clicking **Send** and the **Link** icon:

![image](https://user-images.githubusercontent.com/5924/77241138-67023900-6bab-11ea-8322-17c7009f3891.png)

Put this in the **configuration** section of `index.html` as the value of `REGISTER_FORM_URL`.

*Recommended.* Turn on email notifications for new registrations:

![image](https://user-images.githubusercontent.com/5924/77241236-661dd700-6bac-11ea-944f-0e8dd823be17.png)

## 3. Create another spreadsheet to use as your database of registered businesses

It **MUST** have the following columns, in this order:

- `Business Name`
- `Venmo Handle`
- `Location`
- `Description`
- `GoFundMe URL`

Get the `id` portion of the URL from here:

![image](https://user-images.githubusercontent.com/5924/77240847-09202200-6ba8-11ea-9ee0-1ad714bc12a3.png)

Put this in the **configuration** section of `index.html` as the value of `SPREADSHEET_ID`.

## 4. When people register, verify them and add them to the sheet.

They will automatically show up on your landing site.

## 5. Host your site with GitHub pages

![image](https://user-images.githubusercontent.com/5924/77241254-b39a4400-6bac-11ea-9cf0-0873b7d14174.png)

## 6. You're live!

Optionally setup analytics with the following configuration settings in `index.html`:

```javascript
var GOOGLE_ANALYTICS_ID = '_______';
var FULL_STORY_ORG = '_______';
var FULL_STORY_NAMESPACE = '_______';
```