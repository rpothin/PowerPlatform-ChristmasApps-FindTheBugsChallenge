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

- As a Gifts Manager, I want the gift's assigned quantity to be incremented when one item has been assigned to a child, to be able to correctly track the number of items still available

- As  a Gifts Manager, I want to have a clear view on the gifts (quantity in stock, assigned and available for assignation), to better plan the gifts manufacturing

#### Children management

- As a Children Manager, I want to be able to receive child birth events and having them processed (creation of a record in the Contact table and a related record in the Children's Christmas Present table for the active Christmas Event), to quickly include new children in the Christmas program

- As a Children Manager, I want to be able to quickly and easily identify the age of a child (rounded one year down), to better plan the type of gifts to manufacture

- As a Children Manager, I want children reaching a configured age to be removed from the Christmas program, to be able to focus the effort on the children not the adults

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

- Processing of child birth events with the creation of records
- Assignation of a random gift to a child for the upcoming Christmas
- Mark the children's presents for a gift category as added to Santa Claus' sleigh
- Deactivate children who became to old for this Christmas program

## 🗺 QuickStart Guide

...

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