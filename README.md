# To-do app Accenture Summer Internship 2017

Let's create a todo-app together!

## Useful links

* [Ionic Docs](http://ionicframework.com/docs/intro/installation/)
* [Original Tutorial](https://www.joshmorony.com/build-a-todo-app-from-scratch-with-ionic-2-video-tutorial/) 

## Prerequisites

### Install Chrome

Install [Chrome](https://www.google.com/chrome/browser/desktop/index.html)

### Join Github

Register at [Github](https://github.com/join):

1. Use your Accenture email, _my.name@accenture.com_.
2. Plan: Unlimited public repositories for free.
3. Click "skip this step".

### Configure SSH-key

After successfully registering, visit [Github](https://github.com):

1. Click your avatar at the top right.
2. Select “Settings”.
3. At the left hand side, click “SSH and GPG keys”.
4. Click “New SSH key”.
5. Type “ionic-workshop-key” as title.
6. Add the following key: ```ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDUoGnoNf6EZzyRKtuvzFy0R9hk3Ffdj/6EQKIOvp0/+9Xa6QM7F3e6Fm/i8rX1cE+jJlHu2pmoTTGrJt5kkbkIni95un5Yc5L46LgZF0XCbLofe1Op1jr1mUseQKXFZAFNaqI89BvC1VFtf8b+sUp669Oqkr0cFqbf9TOpZQYGz+U3L37nYabcsjKc6A1LCGBRQLPXsrIrgNpCfDTRkS/2K8GzrZd4Y04es04qzV5LEjs2Hlw0GKwcouCDoX7purT8KKpgBb7w+Bl+rGPVQAdyizkZqivbNrOqg6Zde6mVYPgSjYRMb+IopGQ2R6WuaqDrAfZZ2FV0JCCVfYGa3ZWJ greger.siem.knudsen@CPX-F7KX1V54IV0```
7. Press “Add SSH key”.
8. Open cmd or git bash.
9. Navigate to “C:\Users<your.accenture.id>\Desktop\Repos” or desired location.```cd Repos```
10. Clone the repository by typing: ```git clone git@github.com:gregerKnudsen/ionic-workshop.git```
11. Navigate to repository folder by typing the command:
```
cd ionic-workshop
```

### Install Node

Install [Node.js Current / Latest](https://nodejs.org/en/)

Verify Node installation:

* ```node -v```

* ```npm -v```

### Install Ionic2

Install Ionic2:

```
npm install ionic -g
```

Install Cordova:

```
npm install cordova -g
```

### Install Visual Studio Code

Install [Visual Studio Code](https://nodejs.org/en/) or your favorite IDE

## Creating a simple To-Do app
### Step 1: Creating the home page

1. Generate a new project with a blank template by typing: ```ionic start ionic-todo blank --v2```
2. Open Visual Studio Code. Tip: write the command ```code .``` If this works, skip 3-5.
3. Click “File”
4. Click “Open folder”
5. Select the folder named “ionic-todo” located in “C:\Users\<your.accenture.id\Desktop\repos\ionic-workshop”
6. Open the file “src/pages/home/home.html”. Tip for opening file, inside VSCode press:```CTRL+P``` and write ```home.html``` 
7. Open the command line again, and navigate to the folder ionic-todo: ```cd ionic-todo```
8. Start the application by running: ```ionic serve```. Do not terminate this process, let it run :)
9. Go back to Visual Studio Code rename the page title in the <ion-title> tag to “My Simple ToDo App”:
```html
  	<ion-title>
  		Add To-do
  	</ion-title>
```
10. Add the following under the </ion-title> tag:
```html
	<ion-buttons end>
<button ion-button icon-only (click)="addItem()"><ion-icon name="add-circle"></ion-icon></button>
    	</ion-buttons>
```
And then watch magic happen in the browser :)
11. Replace the <ion-content padding> tag and its contents with the following to-dos container:
```html
 	<ion-content>
  		<ion-list>
    			<ion-item *ngFor="let item of items" 
 			(click)="viewItem(item)">{{item.title}}</ion-item>
  		</ion-list>
</ion-content>
```
12. Open “src/pages/home/home.ts” and under the line “export class HomePage {“, add the following:
```ts
public items;
```
13. In the same file, add the following under the constructor:
```ts
 	ionViewDidLoad(){
    		this.items = [
      			{title: 'hi1', description: 'test1'},
      			{title: 'hi2', description: 'test2'},
      			{title: 'hi3', description: 'test3'}
    		];
 
  	}
 
	addItem(){
  	}
 
  	viewItem(){
  	}
```
14. Save changes, refresh the browser and observe the new to-dos.



### Step 5: Deploy to your own phone
* Register for [Ionic View](https://apps.ionic.io/login)
* Download [Ionic View](http://view.ionic.io/)
* Deploy your app to Ionic View:
* ```ionic serve```
* ```ionic upload```











## Authors

[Greger Siem Knudsen](https://github.com/gregerKnudsen) &
[Anders Langseth](https://github.com/langz)