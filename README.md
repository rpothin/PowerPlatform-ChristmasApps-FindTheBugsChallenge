<p align="center">
    <h1 align="center">
        Power Platform - Christmas Apps - Find the bugs challenge
    </h1>
    <h3 align="center">
        Help Santa Claus find the bugs introduced into the Power Platform applications built to manage Christmas!
    </h3>
</p>

<p align="center">
    <a href="https://github.com/rpothin/PowerPlatform-ChristmasApps-FindTheBugsChallenge/blob/main/LICENSE" alt="Repository License">
        <img src="https://img.shields.io/github/license/rpothin/PowerPlatform-ChristmasApps-FindTheBugsChallenge?color=yellow&label=License" /></a>
    <a href="https://github.com/rpothin/PowerPlatform-ChristmasApps-FindTheBugsChallenge/issues" alt="Open Issues">
        <img src="https://img.shields.io/github/issues-raw/rpothin/PowerPlatform-ChristmasApps-FindTheBugsChallenge?label=Open%20Issues" /></a>
</p>

<p align="center">
    <a href="#watchers" alt="Watchers">
        <img src="https://img.shields.io/github/watchers/rpothin/PowerPlatform-ChristmasApps-FindTheBugsChallenge?style=social" /></a>
    <a href="#forks" alt="Forks">
        <img src="https://img.shields.io/github/forks/rpothin/PowerPlatform-ChristmasApps-FindTheBugsChallenge?style=social" /></a>
    <a href="#stars" alt="Stars">
        <img src="https://img.shields.io/github/stars/rpothin/PowerPlatform-ChristmasApps-FindTheBugsChallenge?style=social" /></a>
</p>

<h3 align="center">
  <a href="https://github.com/rpothin/PowerPlatform-ChristmasApps-FindTheBugsChallenge/issues/new?assignees=rpothin&labels=bug%2Ctriage&template=BUG.yml&title=%5BBug%5D+%3CTitle%3E">Report the bugs</a>
</h3>

## 🎄 The mission 🎄

With Power Platform anyone can build an application, so Santa Claus decided to give it a try to help him manage Christmas. But unfortunately, he did not succeed in making it work, leaving 7 mistakes unresolved. Will you be able to find these mistakes and save Christmas?

### 📖 Santa Claus' requirements

#### Gifts management

- As an Elf, I want to be able to easily track my work (new gift type or add / remove items in the stock for a gift type) directly from the factory line on my mobile device, to give a better near realtime visibility on the gifts in stock

- As a Gifts Production Manager, I want the gift's assigned quantity to be incremented when one item has been assigned to a child, to be able to correctly track the number of items still available

- As  a Gifts Production Manager, I want to have a clear view on the gifts (quantity in stock, assigned and available for assignation), to better plan the gifts manufacturing

#### Children management

- As a Children Data Manager, I want to be able to receive child birth events and having them processed (creation of a record in the Contact table and a related record in the Children's Christmas Present table for the active Christmas Event), to quickly include new children in the Christmas program

- As a Children Data Manager, I want to be able to quickly and easily identify the age of a child (rounded one year down), to better plan the type of gifts to manufacture

- As a Children Data Manager, I want children reaching a configured age to be removed from the Christmas program, to be able to focus the effort on the children not the adults

#### Gifts distribution preparation

- As a Gift Distribution Coordinator, I want to be able to automatically assign a random gift to a child if we have some in stocks, to make this task easier

- As a Gift Distribution Coordinator, I want to be able to get an in-app notification if there is no gift in stock for assignment to a child, to be able to react quickly.

- As a Gift Distribution Coordinator, I want to be able to trigger the assignation of gifts to children when the stock has been refilled, to guarantee a gift for each child

- As a Gift Distribution Coordinator, I want to be able to prepare the gifts to distribute to children in Santa's sleigh based on what have been assigned, to be sure all children will receive their gift for Christmas

### 👀 What's have been built

#### Applications

- A model driven app for a centralized view of the data involved in the management of Christmas
- A canvas app to allow the elves to update the stock of gifts from their mobile
- A canvas app to follow the preparation of the gifts in Santa Claus' sleigh

#### Automation

- Processing of child birth events with the creation of records + cloud flow to easily test this process
- Assignation of a random gift to a child for the upcoming Christmas
- Mark the children's presents for a gift category as added to Santa Claus' sleigh
- Deactivate children who became to old for this Christmas program

## 🗺 QuickStart Guide

### Prerequisites

- A Github account

> **Note**
> If you don't have one, just go to [GitHub sign up page](https://github.com/signup).

- A Power Platform environment with Dataverse

> **Note**
> To obtain a Power Platform environment with Dataverse you can follow one of the methods below:
> - [From the Power Platform Administration Center](https://learn.microsoft.com/en-us/power-platform/admin/create-environment#create-an-environment-with-a-database)
> - [Using the Power Platform CLI](https://learn.microsoft.com/en-us/power-platform/developer/cli/reference/admin#pac-admin-create)
> - [Starting free with a Power Apps Developer Plan](https://powerapps.microsoft.com/en-us/developerplan/)

### Deploy the ChristmasHub solution

- Fork [this repository](https://github.com/rpothin/PowerPlatform-ChristmasApps-FindTheBugsChallenge)

> **Note**
> If you do not know how to do this, you can follow the [Fork a repo](https://docs.github.com/en/get-started/quickstart/fork-a-repo) page of the GitHub documentation.

- In your forked repository, go to the **Settings** tab, then open the **Secrets > Actions** section
- Add the secrets below by clicking on the **New repository secret** green button

> **Note**
> The secrets to create will depend on the way you want to connect to the environnement where you want to import the **ChristmasHub** solution.

| **Authentication method** | **Secrets to create** |
| -- | -- |
| Username - Password | DATAVERSE_ENVIRONMENT_URL <br> ... |
| Cliend ID - Secret | DATAVERSE_ENVIRONMENT_URL <br> TENANT_ID <br> APPLICATION_ID <br> CLIENT_SECRET |

- Still in your forked repository, go the **Code** tab and press the `.` key to open the [**VS Code in the web experience**](https://docs.github.com/en/codespaces/the-githubdev-web-based-editor)
- Open the [configurations/ChristmasHub/DeploymentSettings.json](./configurations/ChristmasHub/DeploymentSettings.json) file and set the elements below
   - **rpo_MaximumChildAge** environment variable value (*ex: 18*)
   - ID of a connection to the Microsoft Dataverse connector in your targeted environment in **rpo_sharedcommondataserviceforapps_c7914**

> **Note**
> To get a connection ID, you can follow the [Get the connection reference information](https://learn.microsoft.com/en-us/power-platform/alm/conn-ref-env-variables-build-tools#get-the-connection-reference-information) from the Microsoft documentation.

- Quit the [**VS Code in the web experience**](https://docs.github.com/en/codespaces/the-githubdev-web-based-editor) and go back to your forked repository
- Go to the **Actions** tab, then open the view on the **import-solution-to-dev** GitHub workflow
- Click on the **Run workflow** button and select the authentication method you want to use to connect to the environnement where you want to import the **ChristmasHub** solution
- Follow the run and when it ends validate that the **ChristmasHub** solution has been correctly imported to your environment

You should now be good to test the applications and reports the 7 bugs you should find 🎄

## ❗ Code of Conduct

I, **Raphael Pothin** ([@rpothin](https://github.com/rpothin)), as creator of this project, am dedicated to providing a welcoming, diverse, and harrassment-free experience for everyone.
I expect everyone visiting or participating in this project to abide by the following [**Code of Conduct**](CODE_OF_CONDUCT.md).
Please read it.

### ✋🏼 Looking for me?

If you have questions or feedbacks regarding this challenge, do not hesitate to contact [@rpothin](https://github.com/rpothin):

- By email at **raphael.pothin@gmail.com**
- On [Twitter](https://twitter.com/RaphaelPothin)

## 📝 License

All files in this repository are subject to the [MIT](LICENSE) license.
