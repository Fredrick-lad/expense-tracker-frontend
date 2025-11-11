# Expense Tracker Frontend Pages Development Schedule

## 📋 Overview
Based on your Spring Boot backend, here's a comprehensive list of pages needed and a suggested development schedule.

---

## 🎯 Phase 1: Authentication & Core Setup (Week 1)

### 1. **Landing/Welcome Page** (`index.html`)
**Priority:** HIGH  
**Time:** 1 day  
**Features:**
- Hero section explaining MONEXA
- Login/Register buttons
- Brief feature highlights
- Responsive design

### 2. **Login Page** (`login.html`)
**Priority:** HIGH  
**Time:** 1 day  
**API Endpoint:** `POST /api/users/login`  
**Features:**
- Username/email input
- Password input
- "Remember me" checkbox
- Link to registration
- Error message display
- Store user data in localStorage/sessionStorage

### 3. **Registration Page** (`register.html`)
**Priority:** HIGH  
**Time:** 1 day  
**API Endpoint:** `POST /api/users/register`  
**Features:**
- Username input (check availability)
- Email input
- Password input
- Confirm password
- Terms & conditions checkbox
- Real-time validation
- Success/error messages

---

## 🏠 Phase 2: Main Dashboard (Week 1-2)

### 4. **Dashboard Page** (`dashboard.html`) ✅ *Already Created*
**Priority:** HIGH  
**Time:** 2 days to complete  
**API Endpoints:**
- `GET /api/expenses?userId={id}` - Get all expenses
- `GET /api/expenses/total?userId={id}` - Get total
**Features to Add:**
- Connect to real API
- Display actual user data
- Calculate today's spending
- Calculate month's spending
- Show recent 5-10 expenses
- Add loading states
- Add empty states

---

## 💰 Phase 3: Expense Management (Week 2)

### 5. **Add Expense Page** (`add-expense.html`)
**Priority:** HIGH  
**Time:** 2 days  
**API Endpoint:** `POST /api/expenses`  
**Features:**
- Amount input (number)
- Date picker (default: today)
- Time picker (default: now)
- Category dropdown (Food, Transport, Entertainment, Bills, etc.)
- Subcategory input (optional)
- Description textarea
- Quick amount buttons (50, 100, 200, 500)
- Submit button
- Success/error feedback
- Option to add another expense

### 6. **Edit Expense Page** (`edit-expense.html`)
**Priority:** MEDIUM  
**Time:** 1 day  
**API Endpoints:**
- `GET /api/expenses/{id}` - Load expense
- `PUT /api/expenses/{id}` - Update expense
**Features:**
- Pre-filled form with existing data
- Same fields as Add Expense
- Update button
- Delete button
- Cancel button

### 7. **Expenses List Page** (`expenses.html`)
**Priority:** HIGH  
**Time:** 2 days  
**API Endpoints:**
- `GET /api/expenses?userId={id}`
- `GET /api/expenses/category?userId={id}&category={name}`
- `DELETE /api/expenses/{id}`
**Features:**
- Searchable/filterable list
- Filter by date range
- Filter by category
- Sort options (date, amount)
- Pagination or infinite scroll
- Edit/delete buttons per item
- Total amount display
- Export option (future)

---

## 🔄 Phase 4: Recurring Expenses (Week 3)

### 8. **Recurring Expenses Dashboard** (`recurring-expenses.html`)
**Priority:** MEDIUM  
**Time:** 2 days  
**API Endpoints:**
- `GET /api/recurring?userId={id}` - Active recurring
- `GET /api/recurring/all?userId={id}` - All recurring
**Features:**
- List of active subscriptions
- Monthly/weekly/daily view
- Total recurring cost per month
- Edit/deactivate buttons
- Add new recurring expense button
- Status indicators (active/inactive)

### 9. **Add/Edit Recurring Expense** (`add-recurring.html`)
**Priority:** MEDIUM  
**Time:** 1 day  
**API Endpoints:**
- `POST /api/recurring`
- `PUT /api/recurring/{id}`
**Features:**
- Amount input
- Category/subcategory
- Description
- Frequency selector (Daily, Weekly, Monthly, Yearly)
- Preferred time picker
- Start date
- Active toggle
- Save button

---

## 📊 Phase 5: Reports & Analytics (Week 3-4)

### 10. **Reports/Analytics Page** (`reports.html`)
**Priority:** MEDIUM  
**Time:** 3 days  
**API Endpoints:**
- `GET /api/expenses/category?userId={id}&category={name}`
- Custom date range queries
**Features:**
- Date range selector
- Spending by category (pie chart)
- Spending trends (line chart)
- Daily/weekly/monthly comparison
- Top spending categories
- Export report button
- Print-friendly view

### 11. **Category Breakdown Page** (`category-details.html`)
**Priority:** LOW  
**Time:** 1 day  
**Features:**
- Detailed view of one category
- All expenses in that category
- Subcategory breakdown
- Trends over time
- Budget vs actual (future feature)

---

## 👤 Phase 6: User Profile & Settings (Week 4)

### 12. **Profile Page** (`profile.html`)
**Priority:** MEDIUM  
**Time:** 2 days  
**API Endpoint:** `GET /api/users/{id}`  
**Features:**
- Display username, email
- Edit profile button (future)
- Change password (future)
- Account statistics
- Member since date
- Delete account option (future)

### 13. **Settings Page** (`settings.html`)
**Priority:** LOW  
**Time:** 1 day  
**Features:**
- Currency selection
- Date format
- Theme toggle (dark/light)
- Notification preferences
- Default categories management
- Export/Import data

---

## 🎨 Phase 7: Supporting Pages (Ongoing)

### 14. **404 Error Page** (`404.html`)
**Priority:** LOW  
**Time:** 2 hours  
**Features:**
- User-friendly error message
- Navigation back to dashboard
- Search functionality

### 15. **Loading/Splash Screen** (if needed)
**Priority:** LOW  
**Time:** 1 hour  
**Features:**
- MONEXA logo animation
- Loading indicator

---

## 📱 Bonus/Future Pages

### 16. **Budget Management** (`budgets.html`)
**Priority:** FUTURE  
**Features:**
- Set monthly budgets per category
- Progress bars
- Alerts when approaching limit

### 17. **Goals/Savings** (`goals.html`)
**Priority:** FUTURE  
**Features:**
- Set savings goals
- Track progress
- Projections

### 18. **Reminders** (`reminders.html`)
**Priority:** FUTURE  
**Features:**
- Set bill payment reminders
- Recurring expense notifications

---

## 📅 Recommended 4-Week Development Schedule

### **Week 1: Foundation**
- Day 1: Landing page
- Day 2: Login page
- Day 3: Registration page
- Day 4-5: Complete Dashboard with API integration

### **Week 2: Core Functionality**
- Day 1-2: Add Expense page
- Day 3: Edit Expense page
- Day 4-5: Expenses List page

### **Week 3: Advanced Features**
- Day 1-2: Recurring Expenses Dashboard
- Day 3: Add/Edit Recurring Expense
- Day 4-5: Start Reports page

### **Week 4: Polish & Additional Pages**
- Day 1-2: Complete Reports page
- Day 3: Profile page
- Day 4: Settings page
- Day 5: Testing, bug fixes, responsive improvements

---

## 🎯 Priority Breakdown

### **Must Have (MVP)**
1. Login Page
2. Registration Page
3. Dashboard
4. Add Expense
5. Expenses List

### **Should Have**
6. Edit Expense
7. Recurring Expenses Dashboard
8. Add Recurring Expense
9. Reports Page

### **Nice to Have**
10. Profile Page
11. Settings Page
12. Category Details
13. Error Pages

### **Future Enhancements**
14. Budget Management
15. Goals/Savings
16. Reminders
17. Export/Import features

---

## 🛠️ Technical Recommendations

### **Shared Components to Build**
- Header/Navigation component
- Sidebar component
- Mobile bottom navigation
- Expense item card
- Loading spinner
- Toast notifications
- Modal dialogs
- Form validation utilities

### **JavaScript Files Needed**
- `api.js` - API communication functions
- `auth.js` - Authentication utilities
- `utils.js` - Helper functions (date formatting, currency, etc.)
- `validation.js` - Form validation
- `chart.js` - Chart rendering (consider Chart.js library)

### **CSS Organization**
- `reset.css` - Browser reset
- `variables.css` - CSS custom properties
- `layout.css` - Grid and flex layouts
- `components.css` - Reusable components
- `pages.css` - Page-specific styles
- `responsive.css` - Media queries

---

## 📝 Notes

1. **API Integration**: Your backend is already built, so focus on connecting frontend to these endpoints
2. **Security**: Store JWT tokens properly if you implement token-based auth
3. **Validation**: Add client-side validation before API calls
4. **Error Handling**: Handle network errors, API errors gracefully
5. **Loading States**: Show loaders during API calls
6. **Empty States**: Design empty states for when users have no data yet
7. **Mobile First**: Your CSS already has mobile support - maintain this
8. **Testing**: Test each page on mobile, tablet, and desktop

---

## ✅ Quick Start Checklist

- [ ] Set up project structure (html/, css/, js/ folders)
- [ ] Create shared API utility functions
- [ ] Build authentication pages (login, register)
- [ ] Connect dashboard to real API
- [ ] Create add/edit expense functionality
- [ ] Build expenses list with filters
- [ ] Add recurring expenses features
- [ ] Create reports/analytics page
- [ ] Add profile and settings
- [ ] Test entire flow end-to-end
- [ ] Deploy frontend and connect to backend

---

**Total Estimated Time:** 4-5 weeks for full feature set (working 4-5 hours/day)