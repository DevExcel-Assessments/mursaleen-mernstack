# mursaleen-mernstack
MERN Stack Developer Assessment 
# MERN-TEST - Mursaleen
**Web E-Commerce Application

## CANDIDATE DETAILS
**NAME: Mursaleen 
**EMAIL: mursaleenumar.pro@gmail.com 
**LAST INTERVIEW: 5th June, 2025

---

## SUBMISSION DETAILS
**START DATE:** 12 June 2025 
**SUBMISSION DEADLINE:** 16 June 2025 

> **NOTE:** We will monitor the submission date from your commit history. We will only review commits made on or before the submission date.  
> **NOTE:** Please provide a **separate README** or a **dedicated section** describing how to run the project locally.

---

## PROJECT OVERVIEW
Build a **web-based E-Commerce application** using **React.js** (and optionally Node.js/Express/MongoDB for advanced functionality). As a senior MERN developer, you’re expected to deliver a **more feature-complete** solution compared to junior-level requirements, including dynamic authentication flows (Login), advanced product listing (filters), a product detail page with static reviews, and a functional cart system.

### Core Scope
1. **Login Screen** (dynamic)  
2. **Sign Up Screen** (static or partially dynamic)  
3. **Forgot Password** (static)  
4. **Home Page (Products Listing + Basic Filtering)**  
5. **Product Detail Page** (with static reviews)  
6. **Add to Cart & Cart Listing**  
7. **Mobile-Responsive** design

> **Optional**: You may build a **custom Node/Express** backend and **MongoDB** if you want a fully custom MERN experience. Otherwise, you can interact directly with the [FakeStoreAPI](https://fakestoreapi.com/docs).

---

## FAKESTOREAPI INTEGRATION
The [FakeStoreAPI](https://fakestoreapi.com/docs) can be used to handle product and cart data. If you opt for a custom backend, replicate or extend these endpoints:

1. **Authentication**  
   - **Login**: `POST https://fakestoreapi.com/auth/login`  
     - Validate user credentials; store token in local storage or cookies.

2. **Products**  
   - **Get Products**: `GET https://fakestoreapi.com/products`  
   - **Get Product by ID**: `GET https://fakestoreapi.com/products/{id}`  

3. **Carts**  
   - **Get Carts by User**: `GET https://fakestoreapi.com/carts`  
   - **Add to Cart**: `POST https://fakestoreapi.com/carts`  
   - **Remove Cart**: `DELETE https://fakestoreapi.com/carts/{id}`  

> **Sign Up**: If you want to implement real sign-up flows, you can mock an API call or adapt it to your own backend.

---

## WEB SCREENS & FEATURES

### 1. Login Screen
![Sign In](https://github.com/user-attachments/assets/acbb774a-ab58-4b06-b06c-6819a6a0178a)

- **API**: `POST /auth/login`  
- **Forms & Validation**: Validate email/password.  
- **Success**: Store token or user details; navigate to **Home Page**.  
- **Failure**: Display user-friendly error messages.

### 2. Sign Up Screen
![Sign Up](https://github.com/user-attachments/assets/f803cbc5-7377-49ba-aad6-751806b1bd60)

- **Optional real API** or **static**.  
- Show a typical registration form (name, email, password, etc.).  
- On successful sign-up, navigate to **Login** or directly to **Home**.

### 3. Forgot Password
![Password Recovery](https://github.com/user-attachments/assets/25f2eca2-1415-498e-a20e-6c893313752c)

- A **static** page (no real back-end flow required).  
- Prompt user for email, display a success message.

### 4. Home Page (Products Listing + Basic Filtering)
![Listing](https://github.com/user-attachments/assets/e349b07b-b0fb-42a2-ad60-b68dbf79afb2)

- **API**: `GET /products` to display items in a **responsive** grid or list.  
- **Filtering**: At least one filter (e.g., category or price range).  
  - `GET /products/categories` or filter logic on the client.  
- Navigate to **Product Detail** on item click.

### 5. Product Detail Page (with Static Reviews)
![Details](https://github.com/user-attachments/assets/c5d12b35-5ddb-4af0-8529-e817030ba9d9)

- **API**: `GET /products/{id}` for product info.  
- **Reviews**: Display mock or static review data.  
- **Add to Cart**: A button that sends a request to `POST /carts` (or local cart logic).

### 6. Cart Listing
![Cart](https://github.com/user-attachments/assets/75d28622-4471-4e7b-bfd4-95d07994cbfc)

- **API**:  
  - `GET /carts` (or local cart in React state).  
  - `DELETE /carts/{id}` to remove items if you integrate with the API.  
- Display product title, price, and quantity.  
- Support removal or quantity changes (optional).

### 7. Mobile-Responsive Design
- Use media queries or a CSS framework (e.g., Tailwind, Bootstrap) to ensure **responsive** layouts for mobile, tablet, and desktop.

---

## FRONT-END REQUIREMENTS (React.js)

1. **React Setup**  
   - Use Create React App (CRA), Vite, or similar.  
   - Leverage **react-router-dom** for page navigation (e.g., `/login`, `/home`, `/cart`).  
2. **State Management**  
   - For a senior-level assignment, consider a structured approach (e.g., **Redux**, **Context API**, or custom hooks).  
   - Handle the auth token (if using real login) and cart state consistently.  
3. **API Calls**  
   - **Axios** or `fetch` for all HTTP requests.  
   - Graceful error handling (e.g., try/catch blocks, user feedback on failure).  
4. **Code Organization & Modularity**  
   - Break down pages, components, services (API calls), and utilities.  
   - Keep consistent naming and file structure.

---

## OPTIONAL BACKEND (FULL MERN)

> If you choose to **showcase a full MERN stack**, you can:
- **Create a Node/Express server** that proxies or mirrors the FakeStoreAPI or uses MongoDB for storing products, carts, and user accounts.  
- **Implement JWT-based auth** on your own endpoints, hooking up the front end to your Node server instead of directly calling FakeStoreAPI.  

This approach can demonstrate your **full-stack** prowess but is not strictly required if you prefer to focus on a robust React front end.

---

## CODE QUALITY MANAGEMENT

- **Clean & Well-Structured Code**  
  - Use meaningful names for components, hooks, and states.
- **Comments & Documentation**  
  - Provide clarity for complex logic or architectural choices.
- **Error Handling & Edge Cases**  
  - Show what happens with empty search results, failed logins, or invalid product IDs.
- **Testing (Optional Bonus)**  
  - Add unit tests or integration tests to highlight your skill.

---

## CODE MANAGEMENT

1. **Git & Commits**  
   - Commit often with clear messages (e.g., `feat: add product filter logic`).
2. **Branching Strategy**  
   - Use feature branches (e.g., `feature/product-detail`) and merge into `main` via Pull Requests.
3. **Pull Requests**  
   - Provide a concise summary of changes with any relevant references.

---

## HOW TO RUN THE APPLICATION LOCALLY

1. **Clone the Repo**  
   ```bash
   git clone https://github.com/{YourRepo}/mern-test.git
   cd mern-test
   ```

2. **Install Dependencies**  
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Start the Application**  
   ```bash
   npm start
   # or
   yarn start
   ```
   - Typically runs at `http://localhost:3000`.

4. **Environment Variables**  
   - If using a .env for API URLs or tokens, specify in your docs (e.g., `REACT_APP_BASE_URL`, etc.).
   - If implementing a custom Node backend, include instructions for starting the server (e.g., `npm run server`).

---

## FIGMA DESIGN
> Provide the **web-based Figma link** here, or attach screenshots for each screen (Login, Home, Detail, Cart, etc.).  (https://www.figma.com/design/cHPdU5ToGD6m2ZFChlACYK/DevExcel-Assement?node-id=0-1&t=DNlrPQB9bUefqQOS-1)
> This ensures candidates can match the intended design. 

---

## GOOD LUCK!
We look forward to your **Senior MERN** solution. If you have any questions, please reach out before the submission deadline.

---

**Happy Coding!**
