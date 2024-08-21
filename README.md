# Link to the Website
https://booking-app-deploy.onrender.com

## NOTE 1:
Payments are currently unavailable as I am using a test version of Stripe.
However, any payment attempts will be captured by the Stripe API and will appear in my Stripe account.
Hence it won't show any error when Confirm Booking Button is pressed to pay.
## NOTE 2:
Kindly Ensure that the Check-in and Check-out dates are not same before proceeding for payment. 


# To run it locally

Have Node.js installed on your system.

## Cloning the Repository

Start by cloning the repository to your local machine:

```bash
git clone https://github.com/AgentAbi/mern-booking-app.git
cd mern-booking-app
```

## Backend Configuration

1. **Environment Files**: Navigate to the `backend` folder and create two files: `.env` and `.env.e2e`. Add the following contents to both files:

    ```plaintext
    MONGODB_CONNECTION_STRING=

    JWT_SECRET_KEY=
    FRONTEND_URL=

    # Cloudinary Variables
    CLOUDINARY_CLOUD_NAME=
    CLOUDINARY_API_KEY=
    CLOUDINARY_API_SECRET=

    # Stripe
    STRIPE_API_KEY=
    ```

2. **MongoDB Setup**: 
    - Sign up for an account at [MongoDB Atlas](https://www.mongodb.com/cloud/atlas).
    - Create a new cluster and follow the instructions to set up a new database.
    - Once set up, obtain your MongoDB connection string and add it to the `MONGODB_CONNECTION_STRING` variable in your `.env` files.
    - For the `.env.e2e` setup see "running automated tests" below

3. **Cloudinary Setup**:
    - Create an account at [Cloudinary](https://cloudinary.com/).
    - Navigate to your dashboard to find your cloud name, API key, and API secret.
    - Add these details to the respective `CLOUDINARY_*` variables in your `.env` files.

4. **Stripe Setup**:
    - Sign up for a Stripe account at [Stripe](https://stripe.com/).
    - Find your API keys in the Stripe dashboard.
    - Add your Stripe API key to the `STRIPE_API_KEY` variable in your `.env` files.
  
5. **JWT_SECRET_KEY**:
    - This just needs to be any long, random string. You can google "secret key generator".

7. **Frontend URL**:
    - The `FRONTEND_URL` should point to the URL where your frontend application is running (typically `http://localhost:5173` if you're running it locally).
  

## Frontend Configuration

1. **Environment Files**: Navigate to the `frontend` folder and create a file: `.env`:

    ```plaintext
    VITE_API_BASE_URL=
    VITE_STRIPE_PUB_KEY=
    ```

5. **VITE_API_BASE_URLL**:
    - The `VITE_API_BASE_URL` should point to the URL where your backend application is running (typically `http://localhost:7000` if you're running it locally).

## Running the Application

1. **Backend**:
    - Navigate to the `backend` directory.
    - Install dependencies: `npm install`.
    - Start the server: `npm start`.

2. **Frontend**:
    - Open a new terminal and navigate to the `frontend` directory.
    - Install dependencies: `npm install`.
    - Start the frontend application: `npm run dev`.
    - The application should now be running on `http://localhost:5173` but verify this in your command line terminal  

