# Elite POI Tutorial App - Planning Document

## Requirements
- **Project**: Elite POI Demo Tutorial App (PWA)
- **Type**: Responsive Mobile + Web prototype for client testing
- **Authentication**: Email/Password only, role-based (Advisor/Admin)
- **Data Import**: Excel file with user credentials (UserID, Password, Role, Name, Email, Mobile, City, State, PinCode, DOB, DateOfJoining)
- **Core Flow**: Login → Profile Setup → Categories → Subcategories → Video Tutorial → Quiz → Certificate
- **Backend**: Supabase for data storage, user management, progress tracking
- **Colors**: Green (#23A455), Orange gradient (#FFB347 → #FF7A00)
- **Tagline**: "Learn POI — Grow Business"

## Design System
- **Primary Colors**: 
  - Green: #23A455 (primary actions, success states)
  - Orange Gradient: #FFB347 → #FF7A00 (CTAs, highlights)
- **Typography**: Clean, professional hierarchy
- **Components**: Modern card-based UI with proper spacing
- **Responsive**: Mobile-first with desktop adaptation

## Database Schema
### Core Collections:
1. **users**: Authentication and profile data
2. **categories**: Main category tiles (6 default)
3. **subcategories**: Category-specific subcategories
4. **topics**: Video tutorials with YouTube URLs
5. **video_progress**: User progress tracking
6. **quizzes**: Quiz definitions
7. **quiz_responses**: User quiz attempts
8. **admin_replies**: Q&A system

## Tasks Breakdown

### Phase 1: Foundation & Authentication (2000 LOC)
- [ ] Setup design system with Elite POI branding
- [ ] Create authentication system (login screen)
- [ ] Implement role-based routing (Advisor/Admin)
- [ ] Setup Supabase database schema
- [ ] Import Excel user data functionality

### Phase 2: Core User Flow (2500 LOC)
- [ ] Profile setup screen (mandatory first-time)
- [ ] Main categories grid (6 tiles)
- [ ] Subcategories navigation
- [ ] Video tutorial player with progress tracking
- [ ] Quiz system (5 MCQ questions)
- [ ] Score card and certificate generation

### Phase 3: Admin Features (1500 LOC)
- [ ] Admin dashboard
- [ ] Category/subcategory CRUD
- [ ] User management and Excel import
- [ ] Mock analytics and reporting
- [ ] Q&A management system

### Phase 4: PWA & Polish (1000 LOC)
- [ ] PWA manifest and service worker
- [ ] Offline capability for app shell
- [ ] Mobile optimization
- [ ] Performance optimization
- [ ] Testing and bug fixes

## Technical Architecture
- **Frontend**: React 18 + TypeScript + React Router
- **Styling**: Tailwind CSS with custom design system
- **Backend**: Supabase (Auth, Database, Storage)
- **State Management**: React Query for server state
- **Video**: YouTube iframe integration
- **PDF**: Client-side certificate generation
- **PWA**: Service worker for offline shell

## Demo Data Requirements
- **Categories**: 6 main tiles (Book New Business, Roll Over, Renewal, Dashboard, My Account, Book Health)
- **Subcategories**: 8 for Book New Business (Two-Wheeler, Private Car, etc.)
- **Video**: Single YouTube tutorial (https://www.youtube.com/watch?v=UxpS1wkHTSA)
- **Quiz**: 5 MCQ questions with explanations
- **Users**: Import from provided Excel file

## Key Features
- **Progress Tracking**: Save video position every 10 seconds
- **Quiz Timing**: Test button appears after 15 minutes of video
- **Certificate**: Auto-generated PDF on course completion
- **Mobile-First**: Responsive design for all screen sizes
- **Role Management**: Separate flows for Advisors and Admins

## Next Steps
1. Setup Supabase project connection
2. Implement design system and authentication
3. Create core user flow screens
4. Add admin functionality
5. Implement PWA features

## Execution Strategy
- Start with authentication and user management
- Build core tutorial flow (video → quiz → certificate)
- Add admin features and analytics
- Polish with PWA capabilities and mobile optimization
- Focus on demo-ready functionality over production features

**Total Estimated LOC**: ~7000 lines
**Estimated Tokens**: ~70,000 tokens