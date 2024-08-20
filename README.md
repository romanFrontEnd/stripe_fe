# Getting Started

Install node version manager on your laptop:
* [Mac](https://medium.com/@priscillashamin/how-to-install-and-configure-nvm-on-mac-os-43e3366c75a6)
* [Windows](https://www.xda-developers.com/how-install-nvm-windows/)
* Install node version v16.16.0: nvm install v16.16.0

### How to Configure

* Open stripe_fe/src/main/App.jsx
* Replace REACT_APP_STRIPE_API_PUBLIC_KEY in .env file
You can pick it up here: [Stripe api key](https://dashboard.stripe.com/test/apikeys)


### Build and run

~~~
npm install
npm run build
~~~

4. Run the client app

~~~
npm run start
~~~

5. Go to [http://localhost:3000/checkout](http://localhost:3000/checkout)

* You should be automatically redirected to checkout page.
* Prebuild item is created during a startup of the application
items: [{ id: "xl-tshirt" , amount: "100"}] see App.jsx

6. How to test 
Please use this cards they are valid for test mode.
* [List of testing Cards](https://docs.stripe.com/payments/accept-a-payment?platform=web&ui=elements&client=react#web-test-the-integration)

* Succesfull payment: 4242424242424242
* Failed payment: 
4000002500003155
* Insufficient funds:
4000000000009995

* Verify webhook response in the server console or in the sripeCli see stripe_be for more details