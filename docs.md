# Idealista Clone - Product Requirements Document

## 1. Product Overview

An Idealista clone is a real estate marketplace platform that connects property buyers, sellers, and renters. The platform enables users to browse, list, search, and manage property listings with advanced filtering, pricing analysis, and user engagement features.

**Target Users:**

- Property sellers/landlords wanting to list properties
- Property buyers/renters searching for properties
- Real estate agents managing multiple listings
- Platform administrators

**Core Value Proposition:**

- Comprehensive real estate marketplace with advanced search and filtering
- Real-time property availability and pricing information
- Secure communication between buyers/sellers
- Detailed property information with photos and virtual tours
- Price history and market analysis tools

---

## 2. Core Functionalities

### 2.1 User Management

- **User Registration & Authentication**
  - Email/password registration
  - Email verification
  - Social login (Google, Facebook)
  - Password reset functionality
  - Two-factor authentication option

- **User Profiles**
  - User account types (Individual buyer, Seller, Real Estate Agent, Admin)
  - Profile completion (name, phone, location, profile picture)
  - Seller verification (ID verification, bank details for payments)
  - User reputation/ratings system
  - Account settings and preferences

### 2.2 Property Listings

- **Create/Manage Listings**
  - Property details (address, location coordinates, property type)
  - Property specifications (bedrooms, bathrooms, square meters, floor, parking)
  - Property features (balcony, garden, furnished, pool, garage, etc.)
  - Listing type (Sale, Rent, Temporary Rent)
  - Price and payment details
  - Lease terms (for rentals)
  - Photo gallery (multiple images with drag-and-drop ordering)
  - Video/Virtual tour integration
  - Property description with rich text editor
  - Contact preference (phone, email, in-app messaging)
  - Listing visibility control (active, inactive, expired)
  - Promotion options (featured, highlighted, priority)

- **Listing Management Dashboard**
  - View all user listings with statistics
  - Edit listing details
  - Renew/extend listing duration
  - Archive/Delete listings
  - View listing views and inquiry counts
  - Promote listings
  - Generate QR codes for listings

### 2.3 Search & Discovery

- **Advanced Search Filters**
  - Location-based search (city, neighborhood, district)
  - Property type filter (apartment, house, land, commercial, etc.)
  - Price range slider
  - Bedrooms/bathrooms filter
  - Square meters range
  - Property features (furnished, garden, garage, etc.)
  - Listing type (sale/rent)
  - Sort options (price, newest, relevance, distance)
  - Search history for authenticated users

- **Map View**
  - Interactive map displaying property locations
  - Cluster markers for density visualization
  - Click to view property details
  - Filter properties shown on map
  - Draw radius search

- **Saved Searches**
  - Save search filters for quick access
  - Alerts for new listings matching saved searches
  - Email notifications for saved search results

### 2.4 Property Details Page

- **Comprehensive Property Information**
  - Full property description and photos
  - Property specifications and features
  - Price history chart
  - Similar properties recommendations
  - Agent/seller information with contact options
  - User reviews and ratings
  - Location details with nearby amenities
  - Energy efficiency rating (if applicable)

- **Interactions**
  - Inquiry form (buyer contacts seller)
  - Schedule viewing/appointment
  - Add to favorites/wishlist
  - Share property (social media, email)
  - Report inappropriate listing

### 2.5 Favorites & Wishlist Management

- **Save Properties**
  - Add/remove properties from favorites
  - Create multiple wishlists with custom names
  - Organize properties by categories
  - Compare selected properties side-by-side
  - Export wishlist (PDF, email)

### 2.6 Messaging & Communication

- **In-App Messaging**
  - Real-time chat between buyers and sellers
  - Message history
  - Typing indicators and read receipts
  - File/document sharing
  - Message notifications

- **Contact Management**
  - Message inbox with conversation threads
  - Archive conversations
  - Block/report users
  - Auto-responses for sellers

### 2.7 Appointments & Viewings

- **Schedule Viewings**
  - Calendar-based appointment scheduling
  - Available time slots for properties
  - Confirmation emails/SMS
  - Reminder notifications
  - Viewing history and notes

### 2.8 Reviews & Ratings

- **User Reviews**
  - Rate sellers/agents (1-5 stars)
  - Written reviews and comments
  - Moderation system for reviews
  - Verified purchase/transaction reviews only
  - Filter reviews by rating

### 2.9 Price Analytics & Market Intelligence

- **Price History**
  - Track price changes over time
  - Price comparison with similar properties
  - Market trends visualization
  - Price per square meter analysis

- **Market Reports** (Admin/Premium)
  - Market statistics by area
  - Average prices by property type
  - Price trends chart
  - Supply and demand analytics

### 2.10 Premium Features

- **Featured Listings**
  - Highlight listings with special badges
  - Featured section on homepage
  - Increased visibility in search results
  - Custom promotion duration

- **Agent/Pro Tools**
  - Bulk listing management
  - Advanced analytics dashboard
  - Lead tracking and CRM
  - Templates for listing descriptions
  - Automated email campaigns
  - Branding customization on listings

### 2.11 Admin Panel

- **Content Management**
  - Manage users and accounts
  - Review and moderate listings
  - Handle user reports and complaints
  - Manage property categories and features
  - Site statistics and analytics

- **Payment Management**
  - Commission tracking
  - Payment processing
  - Financial reports
  - Subscription management for premium users

- **System Configuration**
  - Site settings and configuration
  - Email templates
  - Feature toggles
  - Tax rate management
  - Commission structure

---

## 3. Technical Architecture

### 3.1 Frontend Stack

- **Framework:** React.js or Vue.js
- **State Management:** Redux/Vuex
- **Styling:** Tailwind CSS or Material-UI
- **API Communication:** Axios
- **Map Library:** Google Maps API or Leaflet
- **Image Handling:**
  - Image upload and compression (Sharp.js)
  - CDN integration for serving images (Cloudinary/AWS S3)
- **Real-time Communication:** Socket.io or WebSockets
- **Bundler:** Webpack or Vite

### 3.2 Backend Stack

- **Language:** Node.js (Express.js) or Python (Django/FastAPI)
- **Database:** PostgreSQL (primary), Redis (caching/sessions)
- **Search Engine:** Elasticsearch for property search
- **Authentication:** JWT tokens, bcrypt for passwords
- **File Storage:** AWS S3 or similar CDN
- **Email Service:** SendGrid or AWS SES
- **SMS Service:** Twilio
- **Payment Gateway:** Stripe, PayPal
- **Maps API:** Google Maps API

### 3.3 Deployment & Infrastructure

- **Hosting:** AWS, Google Cloud, or Azure
- **Containerization:** Docker
- **Orchestration:** Kubernetes (optional)
- **CI/CD:** GitHub Actions, GitLab CI
- **Monitoring:** New Relic, DataDog
- **CDN:** CloudFlare, AWS CloudFront

### 3.4 Security

- **Encryption:** SSL/TLS, AES encryption for sensitive data
- **Rate Limiting:** DDoS protection
- **Input Validation:** Server-side validation
- **CSRF Protection:** Token-based CSRF tokens
- **XSS Prevention:** HTML escaping and CSP headers
- **SQL Injection Prevention:** Parameterized queries/ORM
- **API Security:** API key management, OAuth 2.0

---

## 4. User Flows

### 4.1 Buyer User Flow

1. **Discovery Phase**
   - User lands on homepage
   - Browses featured listings
   - Uses search bar or advanced filters
   - Views property on map
   - Clicks on property to view details

2. **Interest Phase**
   - Views property photos and details
   - Reads description and specifications
   - Checks similar properties
   - Adds property to favorites/wishlist
   - Reads reviews of seller/agent

3. **Inquiry Phase**
   - Fills out inquiry form
   - Sends message to seller
   - Receives response notification
   - Schedules viewing appointment

4. **Follow-up**
   - Receives appointment confirmation
   - Attends viewing
   - Rates seller/property
   - May make offer or inquire about other properties

### 4.2 Seller User Flow

1. **Account Setup**
   - User registers and verifies email
   - Completes profile information
   - Verifies identity (if required)

2. **Listing Creation**
   - Clicks "Create Listing" button
   - Fills in property details
   - Uploads photos
   - Adds property description
   - Sets listing price and terms
   - Publishes listing

3. **Listing Management**
   - Monitors listing views and inquiries
   - Responds to buyer messages
   - Schedules viewings
   - Updates listing information if needed
   - Renews or promotes listing
   - Closes listing after sale/rental

4. **Post-Sale**
   - Leaves feedback on buyer
   - May list additional properties

### 4.3 Admin User Flow

1. **Dashboard Overview**
   - Views key metrics and statistics
   - Monitors user activity

2. **Moderation**
   - Reviews reported listings
   - Approves/rejects inappropriate content
   - Manages user complaints

3. **System Management**
   - Configures site settings
   - Manages payment processing
   - Generates financial reports

---

## 5. Database Schema

### 5.1 Core Tables

#### users

```
- id (UUID, Primary Key)
- email (String, Unique, Not Null)
- password_hash (String, Not Null)
- first_name (String)
- last_name (String)
- phone (String)
- profile_picture_url (String)
- user_type (Enum: individual, agent, admin)
- bio (Text)
- location (String)
- is_verified (Boolean, default: false)
- is_active (Boolean, default: true)
- created_at (Timestamp)
- updated_at (Timestamp)
```

#### properties

```
- id (UUID, Primary Key)
- user_id (UUID, Foreign Key -> users)
- title (String, Not Null)
- description (Text)
- property_type (Enum: apartment, house, land, commercial, etc.)
- listing_type (Enum: sale, rent, temporary_rent)
- price (Decimal)
- currency (String, default: EUR)
- bedrooms (Integer)
- bathrooms (Integer)
- area_sqm (Float)
- floor_number (Integer)
- parking_spaces (Integer)
- address (String, Not Null)
- city (String, Not Null)
- district (String)
- postal_code (String)
- latitude (Float)
- longitude (Float)
- features (JSON, array of feature tags)
- is_furnished (Boolean)
- energy_rating (String)
- lease_terms (String, for rentals)
- status (Enum: active, inactive, expired, archived)
- visibility (Enum: public, private, unlisted)
- featured_until (Timestamp)
- views_count (Integer, default: 0)
- inquiries_count (Integer, default: 0)
- created_at (Timestamp)
- updated_at (Timestamp)
- published_at (Timestamp)
- expires_at (Timestamp)
```

#### property_images

```
- id (UUID, Primary Key)
- property_id (UUID, Foreign Key -> properties)
- image_url (String, Not Null)
- thumbnail_url (String)
- display_order (Integer)
- alt_text (String)
- uploaded_at (Timestamp)
```

#### favorites

```
- id (UUID, Primary Key)
- user_id (UUID, Foreign Key -> users)
- property_id (UUID, Foreign Key -> properties)
- wishlist_name (String, default: "My Favorites")
- added_at (Timestamp)
```

#### messages

```
- id (UUID, Primary Key)
- sender_id (UUID, Foreign Key -> users)
- receiver_id (UUID, Foreign Key -> users)
- property_id (UUID, Foreign Key -> properties, Nullable)
- message_content (Text)
- is_read (Boolean, default: false)
- read_at (Timestamp)
- created_at (Timestamp)
```

#### appointments

```
- id (UUID, Primary Key)
- property_id (UUID, Foreign Key -> properties)
- buyer_id (UUID, Foreign Key -> users)
- seller_id (UUID, Foreign Key -> users)
- appointment_date (Datetime)
- status (Enum: pending, confirmed, completed, cancelled)
- notes (Text)
- created_at (Timestamp)
- updated_at (Timestamp)
```

#### reviews

```
- id (UUID, Primary Key)
- reviewer_id (UUID, Foreign Key -> users)
- reviewed_user_id (UUID, Foreign Key -> users)
- property_id (UUID, Foreign Key -> properties, Nullable)
- rating (Integer, 1-5)
- review_text (Text)
- is_verified_transaction (Boolean)
- created_at (Timestamp)
- updated_at (Timestamp)
```

#### price_history

```
- id (UUID, Primary Key)
- property_id (UUID, Foreign Key -> properties)
- previous_price (Decimal)
- new_price (Decimal)
- change_date (Timestamp)
- reason (String)
```

#### saved_searches

```
- id (UUID, Primary Key)
- user_id (UUID, Foreign Key -> users)
- search_name (String)
- filters (JSON, search filter parameters)
- alert_enabled (Boolean, default: true)
- created_at (Timestamp)
```

#### payments

```
- id (UUID, Primary Key)
- user_id (UUID, Foreign Key -> users)
- amount (Decimal)
- currency (String)
- payment_type (Enum: listing_promotion, subscription, commission)
- payment_method (String)
- status (Enum: pending, completed, failed, refunded)
- transaction_id (String)
- created_at (Timestamp)
- updated_at (Timestamp)
```

---

## 6. API Endpoints

### 6.1 Authentication Endpoints

```
POST   /api/auth/register           - Register new user
POST   /api/auth/login              - User login
POST   /api/auth/logout             - User logout
POST   /api/auth/refresh            - Refresh JWT token
POST   /api/auth/forgot-password    - Request password reset
POST   /api/auth/reset-password     - Reset password
POST   /api/auth/verify-email       - Verify email address
POST   /api/auth/social-login       - Social login (Google/Facebook)
```

### 6.2 User Endpoints

```
GET    /api/users/:id               - Get user profile
PUT    /api/users/:id               - Update user profile
POST   /api/users/:id/verify        - Verify user identity
GET    /api/users/:id/listings      - Get user's listings
GET    /api/users/:id/reviews       - Get user reviews
POST   /api/users/:id/avatar        - Upload profile picture
DELETE /api/users/:id/account       - Delete account
```

### 6.3 Property Listing Endpoints

```
GET    /api/properties              - List all properties (with filters)
POST   /api/properties              - Create new property listing
GET    /api/properties/:id          - Get property details
PUT    /api/properties/:id          - Update property
DELETE /api/properties/:id          - Delete property
GET    /api/properties/search/map   - Get properties for map view
POST   /api/properties/:id/images   - Upload property images
DELETE /api/properties/:id/images/:imageId - Delete property image
GET    /api/properties/:id/similar  - Get similar properties
POST   /api/properties/:id/promote  - Promote listing
GET    /api/properties/:id/price-history - Get price history
```

### 6.4 Search & Filter Endpoints

```
GET    /api/search                  - Advanced property search
POST   /api/saved-searches          - Save search filter
GET    /api/saved-searches          - Get user's saved searches
DELETE /api/saved-searches/:id      - Delete saved search
POST   /api/saved-searches/:id/alerts - Toggle search alerts
```

### 6.5 Favorites Endpoints

```
GET    /api/favorites               - Get user's favorites
POST   /api/favorites               - Add property to favorites
DELETE /api/favorites/:propertyId   - Remove from favorites
POST   /api/wishlists              - Create wishlist
GET    /api/wishlists              - Get user's wishlists
PUT    /api/wishlists/:id          - Update wishlist
DELETE /api/wishlists/:id          - Delete wishlist
```

### 6.6 Messaging Endpoints

```
GET    /api/messages/inbox          - Get message inbox
GET    /api/messages/conversation/:userId - Get conversation with user
POST   /api/messages                - Send message
PUT    /api/messages/:id/read       - Mark message as read
DELETE /api/messages/:id            - Delete message
POST   /api/messages/block/:userId  - Block user
```

### 6.7 Appointments Endpoints

```
POST   /api/appointments            - Schedule viewing
GET    /api/appointments            - Get user's appointments
PUT    /api/appointments/:id        - Update appointment
DELETE /api/appointments/:id        - Cancel appointment
GET    /api/appointments/:id/confirm - Confirm appointment
```

### 6.8 Reviews Endpoints

```
GET    /api/reviews/user/:userId    - Get user reviews
POST   /api/reviews                 - Submit review
PUT    /api/reviews/:id             - Update review
DELETE /api/reviews/:id             - Delete review
GET    /api/reviews/property/:propertyId - Get property reviews
```

### 6.9 Analytics Endpoints

```
GET    /api/analytics/market/prices - Get market price data
GET    /api/analytics/property/:id   - Get property analytics
GET    /api/analytics/listing-stats  - Get seller listing statistics
GET    /api/analytics/trends         - Get market trends
```

### 6.10 Admin Endpoints

```
GET    /api/admin/dashboard         - Admin dashboard stats
GET    /api/admin/users             - Manage users
PUT    /api/admin/users/:id         - Update user status
GET    /api/admin/listings          - Moderate listings
PUT    /api/admin/listings/:id/approve - Approve/reject listing
GET    /api/admin/reports           - Get user reports
PUT    /api/admin/reports/:id       - Handle report
GET    /api/admin/payments          - Payment management
GET    /api/admin/analytics         - Platform analytics
```

### 6.11 Payment Endpoints

```
POST   /api/payments/create         - Create payment intent
POST   /api/payments/confirm        - Confirm payment
GET    /api/payments/history        - Get payment history
POST   /api/payments/refund         - Request refund
```

---

## 7. Implementation Notes

### 7.1 Development Phases

**Phase 1: MVP (Core Features)**

- User authentication and profiles
- Basic property listing creation
- Search and filtering
- User messaging system
- Basic appointment scheduling

**Phase 2: Enhancement**

- Map view integration
- Advanced analytics and price history
- Review and rating system
- Wishlist and favorites
- Premium features

**Phase 3: Scale & Optimize**

- Admin panel and moderation
- CRM tools for agents
- Advanced market analytics
- Mobile app development
- Performance optimization

### 7.2 Key Considerations

**Performance:**

- Implement caching for frequently accessed data (Redis)
- Use Elasticsearch for fast property search
- Optimize image delivery with CDN
- Implement pagination for list endpoints
- Database query optimization and indexing

**Scalability:**

- Horizontal scaling with load balancers
- Microservices architecture (optional)
- Message queue for async tasks (RabbitMQ/Kafka)
- Database replication and sharding strategy

**Security:**

- Implement API rate limiting
- Encrypt sensitive data (PII, payment info)
- Regular security audits and penetration testing
- GDPR compliance for user data
- Two-factor authentication for sensitive accounts

**User Experience:**

- Responsive design (mobile-first approach)
- Fast page load times
- Intuitive navigation
- Real-time notifications
- Email digests and alerts

### 7.3 Third-Party Integrations

- **Google Maps API** - Location services and maps
- **Stripe/PayPal** - Payment processing
- **Twilio** - SMS notifications
- **SendGrid** - Email service
- **Cloudinary/AWS S3** - Image storage and CDN
- **Google Auth/Facebook SDK** - Social login
- **Google Analytics** - User analytics

### 7.4 Testing Strategy

- **Unit Testing:** Jest/Mocha for backend and frontend
- **Integration Testing:** API endpoint testing
- **E2E Testing:** Selenium/Cypress for user flows
- **Performance Testing:** Load testing with JMeter
- **Security Testing:** OWASP vulnerability scanning

### 7.5 Monitoring & Analytics

- **Error Tracking:** Sentry
- **Performance Monitoring:** New Relic or DataDog
- **Analytics:** Google Analytics, Mixpanel
- **Logging:** ELK Stack (Elasticsearch, Logstash, Kibana)

### 7.6 Future Enhancements

- Virtual property tours (360° photos, video tours)
- AI-powered property recommendations
- Mortgage calculator integration
- Property valuation tool
- Blockchain-based property verification
- Cryptocurrency payment options
- Augmented Reality property visualization
- Mobile native apps (iOS/Android)
- Chatbot for instant support
