# Smart India Hackathon Workshop
Date: November 10, 2026  
Reference Number: SIH 26033  
Problem Title: Multiple intermediaries reduce farmers earnings and increase consumer prices.  
Problem Creator's Organization: Ministry of Consumer Affairs, Food & Public Distribution  
Theme: Agriculture, FoodTech & Rural Development  

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

 =>Problem Description
- Create a digital marketplace that:
- Connects farmers/FPOs directly with consumers and bulk buyers.
- Provides logistics support.
- Uses AI for demand forecasting and route optimization.

=>Benefits:
- Better prices for farmers.
- Lower prices for consumers.
- Reduced supply chain inefficiencies.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Proposed Solution

1. Direct Multi-Tier Marketplace:  
   An integrated mobile and web platform connecting individual farmers and Farmer Producer Organizations (FPOs) directly with bulk institutional buyers (retailers, hotels, canteens) and retail consumers, bypassing commission agents and multi-layer traders.

2. PostGIS(Geographic Information System) Order Aggregation & Logistics Support: 
   A spatial clustering system that aggregates small-scale harvests from nearby smallholder farms into single consolidated pickup loads. Integrated local transport dispatch arranges last-mile and mid-mile transit directly from farm-gate to distribution hubs.

3. AI Demand & Price Forecasting with Route Optimization:  
   AI models predict localized produce demand and price fluctuations using Agmarknet historical trends and platform order history. Integrated route optimization algorithms calculate efficient collection paths for logistics drivers to minimize transit delays and fuel costs.

4. Innovation & Uniqueness:
   Unlike generic e-commerce platforms or basic price aggregators, this solution focuses on **hyper-local micro-logistics and order aggregation for smallholder farmers**, ensuring affordable transport economics while maintaining a transparent escrow-backed payment structure upon quality verification.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Technical Approach

- Technologies & Stack
- Frontend: Flutter (multilingual, low-bandwidth mobile app for farmers/drivers), Next.js / React (web dashboard for FPOs, bulk buyers, admins)
- Backend: Python FastAPI / Node.js
- Database & GIS: PostgreSQL with **PostGIS** extension for spatial geolocation querying and regional cluster analysis
- AI & Optimization: Python (`Google OR-Tools` for Vehicle Routing Problems with Time Windows - VRPTW; `Prophet` / `LSTM` models for Agmarknet price and demand forecasting)
- Payments & Security: Escrow-based payment integration (UPI / Razorpay / Net Banking) with automated milestone releases upon FPO quality confirmation

### Implementation Flow

```text
 [ Farmers / FPOs ]
        │
        ▼
[ Order Aggregation Engine ] (PostGIS Spatial Radius Querying)
        │
        ▼
[ AI Demand & Price Engine ] (Agmarknet Trend Analysis)
        │
        ▼
[ Direct Marketplace Hub ] ◄─── [ Bulk Buyers / Consumers ]
        │
        ▼
[ Route Optimization (VRPTW) ] (Google OR-Tools)
        │
        ▼
[ Farm-Gate Pickup & Delivery ] ──► [ Escrow Payout to Farmers ]
