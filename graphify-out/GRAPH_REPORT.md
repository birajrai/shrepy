# Graph Report - .  (2026-07-18)

## Corpus Check
- 367 files · ~229,558 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 2256 nodes · 4261 edges · 230 communities (153 shown, 77 thin omitted)
- Extraction: 99% EXTRACTED · 1% INFERRED · 0% AMBIGUOUS · INFERRED: 33 edges (avg confidence: 0.55)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- Store Management API
- Store Management API
- Storefront UI Components
- Payment Gateways & DTOs
- Merchant Dashboard Routes
- Merchant Dashboard Routes
- Store Management API
- Order Management API
- Internal Admin Dependencies
- Shared Common Package
- Product & Catalog API
- Product & Catalog API
- Order Management API
- Marketing Website Frontend
- Payment Gateways & DTOs
- Database Schema Definitions
- Product & Catalog API
- App Dependencies
- Module: Module
- Internal Admin Interface
- Product & Catalog API
- Product & Catalog API
- Product & Catalog API
- Internal Admin Interface
- Module: Module
- Marketing Website Frontend
- Database Schema Definitions
- Module: Controller
- Payment Gateways & DTOs
- App Dependencies
- Marketing Website Frontend
- Module: Controller
- Payment Gateways & DTOs
- Order Management API
- Shared Common Package
- Marketing Website Frontend
- Merchant Dashboard Routes
- Backend Dependencies
- Merchant Dashboard Routes
- Product & Catalog API
- Module: Controller
- Payment Gateways & DTOs
- Marketing Website Frontend
- Shared Common Package
- Payment Gateways & DTOs
- Shared Common Package
- Marketing Website Frontend
- Marketing Website Frontend
- Merchant Dashboard Routes
- Shared Common Package
- Customer Database Schemas
- Shared Common Package
- Payment Gateways & DTOs
- Shared Common Package
- Payment Gateways & DTOs
- App Dependencies
- Dashboard Core Components
- Merchant Dashboard Routes
- Module: Controller
- Merchant Dashboard Routes
- Merchant Dashboard Routes
- Module: Dto
- Marketing Website Frontend
- Merchant Dashboard Routes
- Module: Dto
- Payment Gateways & DTOs
- Payment Gateways & DTOs
- Payment Gateways & DTOs
- Marketing Website Frontend
- Database Schema Definitions
- Community 70
- Merchant Dashboard Routes
- Database Schema Definitions
- Marketing Website Frontend
- Backend Dependencies
- Dashboard Core Components
- Merchant Dashboard Routes
- Merchant Dashboard Routes
- Backend Dependencies
- Payment Gateways & DTOs
- Payment Gateways & DTOs
- Payment Gateways & DTOs
- Shared Common Package
- Marketing Website Frontend
- Internal Admin Interface
- Internal Admin Interface
- Internal Admin Interface
- Merchant Dashboard Routes
- Community 88
- Database Schema Definitions
- Community 90
- Payment Gateways & DTOs
- Community 92
- Internal Admin Interface
- Shared Common Package
- Shared Common Package
- Shared Common Package
- Shared Common Package
- Database Schema Definitions
- Backend Dependencies
- Payment Gateways & DTOs
- Shared Common Package
- Shared Common Package
- Community 111
- Shared Common Package
- Shared Common Package
- Shared Common Package
- Shared Common Package
- Shared Common Package
- Shared Common Package
- Shared Common Package
- Shared Common Package
- Backend Dependencies
- Backend Dependencies
- Backend Dependencies
- App Dependencies
- App Dependencies
- App Dependencies
- Backend Dependencies
- App Dependencies
- App Dependencies
- Backend Dependencies
- Backend Dependencies
- Backend Dependencies
- Backend Dependencies
- Backend Dependencies
- Backend Dependencies
- App Dependencies
- App Dependencies
- App Dependencies
- App Dependencies
- App Dependencies
- App Dependencies
- App Dependencies
- App Dependencies
- App Dependencies
- App Dependencies
- App Dependencies
- App Dependencies
- Backend Dependencies
- Backend Dependencies
- Database Schema Definitions
- Backend Dependencies
- Backend Dependencies
- Backend Dependencies
- Backend Dependencies
- App Dependencies
- Backend Dependencies
- App Dependencies
- App Dependencies
- App Dependencies
- App Dependencies
- App Dependencies
- App Dependencies
- Shared Common Package
- App Dependencies
- App Dependencies
- App Dependencies
- App Dependencies
- App Dependencies
- App Dependencies
- App Dependencies
- Backend Dependencies
- Backend Dependencies
- Backend Dependencies
- Backend Dependencies
- Backend Dependencies
- Backend Dependencies
- Backend Dependencies
- Backend Dependencies
- Backend Dependencies
- Backend Dependencies
- Backend Dependencies
- Backend Dependencies
- Backend Dependencies
- Shared Common Package
- Shared Common Package
- Shared Common Package

## God Nodes (most connected - your core abstractions)
1. `getDb()` - 132 edges
2. `StoreId` - 58 edges
3. `ProductController` - 36 edges
4. `Post` - 33 edges
5. `FileRoutesByPath` - 30 edges
6. `GeoService` - 29 edges
7. `Public()` - 28 edges
8. `GeoController` - 28 edges
9. `OrderService` - 26 edges
10. `PaymentGateway` - 25 edges

## Surprising Connections (you probably didn't know these)
- `bootstrap()` --indirect_call--> `AppModule`  [INFERRED]
  shrepy-backend/src/main.ts → shrepy-backend/src/app.module.ts
- `ListProductsResult` --references--> `ProductRecord`  [EXTRACTED]
  shrepy-backend/src/modules/product/product.service.ts → shrepy-backend/src/constants.ts
- `FileRoutesByPath` --references--> `Route`  [EXTRACTED]
  shrepy-app/app/routeTree.gen.ts → shrepy-app/app/routes/dashboard.appearance.tsx
- `FileRoutesByPath` --references--> `Route`  [EXTRACTED]
  shrepy-app/app/routeTree.gen.ts → shrepy-app/app/routes/dashboard.brands.tsx
- `FileRoutesByPath` --references--> `Route`  [EXTRACTED]
  shrepy-app/app/routeTree.gen.ts → shrepy-app/app/routes/dashboard.categories.tsx

## Import Cycles
- None detected.

## Communities (230 total, 77 thin omitted)

### Community 0 - "Store Management API"
Cohesion: 0.05
Nodes (30): StoreWithPlan, CreateStoreDto, InviteStaffDto, SwitchStoreDto, IsBoolean, IsNotEmpty, IsOptional, IsString (+22 more)

### Community 1 - "Store Management API"
Cohesion: 0.06
Nodes (50): ApiProperty, ApiQuery, IsEmail, MinLength, HealthController, ApiOperation, ApiTags, Controller (+42 more)

### Community 2 - "Storefront UI Components"
Cohesion: 0.07
Nodes (43): CartDrawer(), Footer(), Header(), ProductCard(), CartContext, CartItem, CartProvider(), CartState (+35 more)

### Community 3 - "Payment Gateways & DTOs"
Cohesion: 0.05
Nodes (31): Catch, Global, AppModule, Module, CommonModule, Module, GlobalExceptionFilter, AuthGuard (+23 more)

### Community 4 - "Merchant Dashboard Routes"
Cohesion: 0.04
Nodes (47): queryClient, Register, router, @tanstack/react-router, Route, Route, Route, DashboardAppearanceRoute (+39 more)

### Community 5 - "Merchant Dashboard Routes"
Cohesion: 0.08
Nodes (24): api, Button(), ButtonProps, Card(), CardProps, Route, CategoryNode, Route (+16 more)

### Community 6 - "Store Management API"
Cohesion: 0.07
Nodes (37): account, accountRelations, session, sessionRelations, user, userRelations, verification, businessVerification (+29 more)

### Community 7 - "Order Management API"
Cohesion: 0.08
Nodes (13): OrderController, Body, Controller, Delete, Get, HttpCode, Param, Put (+5 more)

### Community 8 - "Internal Admin Dependencies"
Cohesion: 0.04
Nodes (47): dependencies, clsx, isbot, lucide-react, react, react-dom, react-router, @react-router/node (+39 more)

### Community 9 - "Shared Common Package"
Cohesion: 0.04
Nodes (47): dependencies, clsx, isbot, lucide-react, react, react-dom, react-router, @react-router/node (+39 more)

### Community 10 - "Product & Catalog API"
Cohesion: 0.15
Nodes (11): StoreId, ProductController, Body, Controller, Delete, Get, HttpCode, Param (+3 more)

### Community 11 - "Product & Catalog API"
Cohesion: 0.11
Nodes (28): OptionTypeRecord, PriceRecord, ProductPublication, ProductVariant, media, optionType, optionValue, optionValueVariant (+20 more)

### Community 12 - "Order Management API"
Cohesion: 0.06
Nodes (35): customer, customerAddress, customerSession, fulfillmentStatusEnum, order, orderItem, orderItemRelations, orderRelations (+27 more)

### Community 13 - "Marketing Website Frontend"
Cohesion: 0.05
Nodes (41): autoprefixer, gray-matter, postcss, react-helmet-async, react-markdown, react-router-dom, dependencies, gray-matter (+33 more)

### Community 14 - "Payment Gateways & DTOs"
Cohesion: 0.09
Nodes (20): ApiBearerAuth, CurrentUser, SavePaymentSettingsDto, IsBoolean, IsOptional, IsString, TestConnectionDto, IsNotEmpty (+12 more)

### Community 15 - "Database Schema Definitions"
Cohesion: 0.09
Nodes (20): CustomFieldType, MediaItem, OptionTypeKind, OptionValueRecord, parseStorageBytes(), PLAN_LIMITS, PlanLimits, ProductDescriptionDocument (+12 more)

### Community 16 - "Product & Catalog API"
Cohesion: 0.08
Nodes (30): CustomFieldRecord, ProductMedia, ProductStatus, brandRelations, categoryRelations, collectionRelations, customField, customFieldRelations (+22 more)

### Community 17 - "App Dependencies"
Cohesion: 0.06
Nodes (30): devDependencies, @react-router/dev, tailwindcss, @tailwindcss/vite, @tanstack/router-plugin, @types/node, @types/react, @types/react-dom (+22 more)

### Community 18 - "Module: Module"
Cohesion: 0.07
Nodes (29): app/**/*, app/routeTree.gen.ts, build, node, compilerOptions, esModuleInterop, jsx, lib (+21 more)

### Community 19 - "Internal Admin Interface"
Cohesion: 0.08
Nodes (16): AdminAlert, AdminAuditLog, AdminUser, AdminWebhookLog, BusinessVerification, DashboardData, GeoCountry, GeoCurrency (+8 more)

### Community 20 - "Product & Catalog API"
Cohesion: 0.14
Nodes (14): BrandRecord, BrandWithCount, CategoryRecord, CategoryWithCount, brand, category, BrandService, Injectable (+6 more)

### Community 21 - "Product & Catalog API"
Cohesion: 0.27
Nodes (28): BulkDeleteDto, BulkStatusDto, CreateBrandDto, CreateCategoryDto, CreateCollectionDto, CreateOptionTypeDto, CreateProductDto, CreateVariantDto (+20 more)

### Community 22 - "Product & Catalog API"
Cohesion: 0.12
Nodes (17): CollectionRecord, CollectionWithCount, appearance, appearanceRelations, design, designPage, designPageRelations, designRelations (+9 more)

### Community 23 - "Internal Admin Interface"
Cohesion: 0.08
Nodes (26): compilerOptions, baseUrl, esModuleInterop, forceConsistentCasingInFileNames, jsx, lib, module, moduleResolution (+18 more)

### Community 24 - "Module: Module"
Cohesion: 0.08
Nodes (26): compilerOptions, baseUrl, esModuleInterop, forceConsistentCasingInFileNames, jsx, lib, module, moduleResolution (+18 more)

### Community 25 - "Marketing Website Frontend"
Cohesion: 0.08
Nodes (19): AcceptableUse, Blog, CookiePolicy, Dmca, Grievance, IpPolicy, KycPolicy, PaymentsPolicy (+11 more)

### Community 26 - "Database Schema Definitions"
Cohesion: 0.15
Nodes (20): country, countryRelations, currency, region, regionRelations, state, stateRelations, CreateCountryDto (+12 more)

### Community 27 - "Module: Controller"
Cohesion: 0.17
Nodes (7): Patch, GeoController, Controller, Delete, Get, Param, Query

### Community 28 - "Payment Gateways & DTOs"
Cohesion: 0.09
Nodes (23): @aws-sdk/client-s3, better-auth, class-transformer, @nestjs/common, @nestjs/core, @nestjs/platform-express, @nestjs/throttler, razorpay (+15 more)

### Community 29 - "App Dependencies"
Cohesion: 0.09
Nodes (22): compilerOptions, allowSyntheticDefaultImports, baseUrl, declaration, emitDecoratorMetadata, esModuleInterop, experimentalDecorators, forceConsistentCasingInFileNames (+14 more)

### Community 30 - "Marketing Website Frontend"
Cohesion: 0.12
Nodes (3): Header(), navLinks, siteConfig

### Community 32 - "Payment Gateways & DTOs"
Cohesion: 0.21
Nodes (8): CashfreeCredentials, CashfreeGateway, PaytmCredentials, PhonePeCredentials, CreateOrderInput, CreateOrderResult, generateSandboxFallback(), getBaseUrl()

### Community 33 - "Order Management API"
Cohesion: 0.29
Nodes (18): AddressDto, BulkDeleteOrdersDto, BulkUpdateOrdersDto, CartItemDto, CreateOrderDto, LookupOrderDto, IsArray, IsIn (+10 more)

### Community 34 - "Shared Common Package"
Cohesion: 0.16
Nodes (18): CountryData, CURRENCY, CURRENCY_SYMBOL, CURRENCY_VALUES, CurrencyData, formatCurrency(), formatCurrencyWithSymbol(), formatDate() (+10 more)

### Community 35 - "Marketing Website Frontend"
Cohesion: 0.17
Nodes (10): FPDF, HTMLParser, clean_and_parse_jsx(), clean_text_for_pdf(), create_cover_page(), get_matching_div(), HTMLToMarkdownParser, main() (+2 more)

### Community 36 - "Merchant Dashboard Routes"
Cohesion: 0.12
Nodes (12): Badge(), BadgeProps, classes, brandColors, fontList, ratioOptions, Route, ProductsSearch (+4 more)

### Community 37 - "Backend Dependencies"
Cohesion: 0.11
Nodes (18): scripts, build, db:generate, db:migrate, db:push, db:studio, format, lint (+10 more)

### Community 38 - "Merchant Dashboard Routes"
Cohesion: 0.15
Nodes (11): authClient, AuthMode, AuthSurface(), AuthSurfaceProps, normalizePhone(), Route, Route, Route (+3 more)

### Community 39 - "Product & Catalog API"
Cohesion: 0.26
Nodes (5): ProductRecord, normalizeMediaInput(), parseDate(), ProductService, Injectable

### Community 40 - "Module: Controller"
Cohesion: 0.17
Nodes (10): MediaController, Controller, Delete, Get, HttpCode, Param, Query, Res (+2 more)

### Community 41 - "Payment Gateways & DTOs"
Cohesion: 0.15
Nodes (7): CCAvenueCredentials, CCAvenueGateway, RazorpayClient, RazorpayCredentials, RazorpayGateway, VerifyPaymentInput, safeCompare()

### Community 42 - "Marketing Website Frontend"
Cohesion: 0.20
Nodes (4): buildWebPageLd(), fullUrl(), SEO(), Contact()

### Community 43 - "Shared Common Package"
Cohesion: 0.13
Nodes (14): src/**/*, compilerOptions, declaration, esModuleInterop, forceConsistentCasingInFileNames, module, moduleResolution, outDir (+6 more)

### Community 44 - "Payment Gateways & DTOs"
Cohesion: 0.29
Nodes (7): getDb(), auth, TODO: integrate with email service (Phase 14), AuthenticatedRequest, createPaymentIntegration(), getPaymentIntegration(), updatePaymentIntegration()

### Community 45 - "Shared Common Package"
Cohesion: 0.13
Nodes (11): BILLING_PLAN_KEYS, BILLING_PLANS, BillingPlan, BillingPlanKey, BillingPlanLimits, BillingPlanSeed, PaidBillingPlan, PlanPricingSettings (+3 more)

### Community 46 - "Marketing Website Frontend"
Cohesion: 0.17
Nodes (11): Footer(), footerLinks, socialIcons, breadcrumbLd(), breadcrumbMap, homeCrumb, Layout(), navLd() (+3 more)

### Community 47 - "Marketing Website Frontend"
Cohesion: 0.19
Nodes (10): Hero(), FaqSection(), FEATURES_LIST, HOME_FAQS, INTEGRATIONS, faqLd(), Home(), howToLd (+2 more)

### Community 48 - "Merchant Dashboard Routes"
Cohesion: 0.18
Nodes (11): APPEARANCE_COLOR_SHADES, APPEARANCE_FONT_LIST, APPEARANCE_RATIO_OPTIONS, CACHE, ENV_KEY, ONBOARDING_CATEGORIES, ONBOARDING_COUNTRIES, ONBOARDING_CURRENCY_VALUES (+3 more)

### Community 49 - "Shared Common Package"
Cohesion: 0.20
Nodes (10): APP, ERROR, HTTP_STATUS, cn(), formatCurrency(), formatDate(), formatDateTime(), formatINR() (+2 more)

### Community 50 - "Customer Database Schemas"
Cohesion: 0.15
Nodes (12): shrepyAuditLog, shrepyCustomer, shrepyCustomerAddress, shrepyCustomerAddressRelations, shrepyCustomerConsent, shrepyCustomerDevice, shrepyCustomerNotification, shrepyCustomerPreference (+4 more)

### Community 51 - "Shared Common Package"
Cohesion: 0.17
Nodes (12): **/*.(t|j)s, jest, collectCoverageFrom, coverageDirectory, moduleNameMapper, rootDir, testEnvironment, testRegex (+4 more)

### Community 52 - "Payment Gateways & DTOs"
Cohesion: 0.18
Nodes (3): StripeCredentials, StripeGateway, PaymentGateway

### Community 53 - "Shared Common Package"
Cohesion: 0.17
Nodes (11): files, dist, license, main, name, private, publishConfig, registry (+3 more)

### Community 54 - "Payment Gateways & DTOs"
Cohesion: 0.29
Nodes (10): getPaymentGatewaysForCountry(), PAYMENT_GATEWAYS, PAYMENT_METHOD, PAYMENT_METHOD_VALUES, PAYMENT_STATUS, PAYMENT_STATUS_VALUES, PaymentGateway, PaymentMethod (+2 more)

### Community 55 - "App Dependencies"
Cohesion: 0.18
Nodes (11): chart.js, @dnd-kit/utilities, @mantine/carousel, dependencies, chart.js, @dnd-kit/utilities, @mantine/carousel, @react-router/node (+3 more)

### Community 57 - "Merchant Dashboard Routes"
Cohesion: 0.18
Nodes (8): blockLabels, BlockNode, defaultFooter, defaultHeader, defaultTemplates, HistoryState, Route, SectionInstance

### Community 58 - "Module: Controller"
Cohesion: 0.25
Nodes (3): Body, HttpCode, Put

### Community 59 - "Merchant Dashboard Routes"
Cohesion: 0.20
Nodes (6): EmptyStateProps, fulfillmentColors, OrdersSearch, paymentColors, Route, statusOptions

### Community 60 - "Merchant Dashboard Routes"
Cohesion: 0.24
Nodes (6): MerchantShell(), MerchantShellProps, navItems, Sidebar(), SidebarProps, Route

### Community 61 - "Module: Dto"
Cohesion: 0.31
Nodes (7): CreateCurrencyDto, IsBoolean, IsInt, IsNotEmpty, IsOptional, IsString, UpdateCurrencyDto

### Community 62 - "Marketing Website Frontend"
Cohesion: 0.24
Nodes (3): routes, ErrorBoundary, ScrollToTop()

### Community 63 - "Merchant Dashboard Routes"
Cohesion: 0.31
Nodes (8): DashboardIndex(), formatExactDate(), formatRelativeTime(), formatStatusLabel(), OrderTrendPeriod, quickActions, Route, statusTone

### Community 64 - "Module: Dto"
Cohesion: 0.33
Nodes (6): CreateStateDto, IsBoolean, IsNotEmpty, IsOptional, IsString, UpdateStateDto

### Community 67 - "Payment Gateways & DTOs"
Cohesion: 0.22
Nodes (4): KhaltiConfig, KhaltiCredentials, KhaltiGateway, KhaltiVerificationResponse

### Community 68 - "Marketing Website Frontend"
Cohesion: 0.31
Nodes (8): buildXml(), __dirname, getBlogPages(), main(), publicDir, root, staticPages, urlXml()

### Community 69 - "Database Schema Definitions"
Cohesion: 0.25
Nodes (7): type, url, instructions, mcp, context7, $schema, AGENTS.md

### Community 70 - "Community 70"
Cohesion: 0.25
Nodes (7): **/*spec.ts, test, ./tsconfig.json, exclude, extends, dist, node_modules

### Community 71 - "Merchant Dashboard Routes"
Cohesion: 0.25
Nodes (6): businessCategories, countryBusinessTypes, countryStates, DocState, monthlySalesOptionsByCountry, Route

### Community 72 - "Database Schema Definitions"
Cohesion: 0.25
Nodes (7): adminAlert, adminAlertRelations, adminAuditLog, adminAuditLogRelations, adminNote, adminNoteRelations, adminWebhookLog

### Community 73 - "Marketing Website Frontend"
Cohesion: 0.25
Nodes (5): __dirname, gradientBuffer, logoX, logoY, root

### Community 74 - "Backend Dependencies"
Cohesion: 0.29
Nodes (7): drizzle-kit, @eslint/js, devDependencies, drizzle-kit, @eslint/js, ts-node, ts-node

### Community 76 - "Merchant Dashboard Routes"
Cohesion: 0.33
Nodes (4): Placeholder(), MyRouterContext, Route, FileRoutesById

### Community 77 - "Merchant Dashboard Routes"
Cohesion: 0.43
Nodes (6): DiscountPayload, DiscountsComponent(), Route, statusLabel(), statusTone(), toISODate()

### Community 78 - "Backend Dependencies"
Cohesion: 0.29
Nodes (6): author, description, license, name, private, version

### Community 79 - "Payment Gateways & DTOs"
Cohesion: 0.48
Nodes (5): createGateway(), getAvailablePaymentMethods(), getPaymentKeySecret(), getPaymentPublicKeyId(), PAYMENT_METHOD

### Community 81 - "Payment Gateways & DTOs"
Cohesion: 0.43
Nodes (5): hasAtLeastOnePaymentMethod(), isPaymentMethodEnabled(), supportsOnlinePayments(), PaymentSettingsState, StorePaymentCredentials

### Community 82 - "Shared Common Package"
Cohesion: 0.29
Nodes (7): import, types, exports, ./app, ./http, import, types

### Community 83 - "Marketing Website Frontend"
Cohesion: 0.33
Nodes (6): contentDir, __dirname, main(), outDir, parsePosts(), root

### Community 84 - "Internal Admin Interface"
Cohesion: 0.60
Nodes (5): adminDelete(), adminFetch(), adminGet(), adminPost(), adminPut()

### Community 86 - "Internal Admin Interface"
Cohesion: 0.33
Nodes (5): fs, local, path, pkg, pkgPath

### Community 87 - "Merchant Dashboard Routes"
Cohesion: 0.40
Nodes (4): formatCurrencyAmount(), planLabels, Route, SubscriptionComponent()

### Community 88 - "Community 88"
Cohesion: 0.33
Nodes (5): fs, local, path, pkg, pkgPath

### Community 89 - "Database Schema Definitions"
Cohesion: 0.33
Nodes (5): collection, compilerOptions, deleteOutDir, $schema, sourceRoot

### Community 90 - "Community 90"
Cohesion: 0.33
Nodes (5): fs, local, path, pkg, pkgPath

### Community 92 - "Community 92"
Cohesion: 0.33
Nodes (5): fs, local, path, pkg, pkgPath

### Community 94 - "Shared Common Package"
Cohesion: 0.40
Nodes (5): devDependencies, typescript, vitest, typescript, vitest

### Community 95 - "Shared Common Package"
Cohesion: 0.40
Nodes (5): scripts, build, prepublishOnly, test, test:watch

### Community 96 - "Shared Common Package"
Cohesion: 0.40
Nodes (4): DISCOUNT_APPLIES_TO, DISCOUNT_APPLIES_TO_VALUES, DISCOUNT_TYPE, DISCOUNT_TYPE_VALUES

### Community 97 - "Shared Common Package"
Cohesion: 0.40
Nodes (4): PAGE_TYPE, PAGE_TYPE_VALUES, PRODUCT_STATUS, PRODUCT_STATUS_VALUES

### Community 98 - "Database Schema Definitions"
Cohesion: 0.50
Nodes (3): plugin, $schema, .opencode/plugins/graphify.js

### Community 99 - "Backend Dependencies"
Cohesion: 0.50
Nodes (4): js, json, moduleFileExtensions, ts

### Community 109 - "Shared Common Package"
Cohesion: 0.50
Nodes (3): FULFILLMENT_STATUS, FULFILLMENT_STATUS_VALUES, FulfillmentStatus

### Community 110 - "Shared Common Package"
Cohesion: 0.50
Nodes (3): PLACEMENT_ZONE, SECTION_TYPE, SETTING_TYPE

### Community 126 - "Shared Common Package"
Cohesion: 0.67
Nodes (3): import, types, ./billing

### Community 127 - "Shared Common Package"
Cohesion: 0.67
Nodes (3): import, types, ./currency

### Community 128 - "Shared Common Package"
Cohesion: 0.67
Nodes (3): import, types, ./discount

### Community 129 - "Shared Common Package"
Cohesion: 0.67
Nodes (3): ./fulfillment, import, types

### Community 130 - "Shared Common Package"
Cohesion: 0.67
Nodes (3): ./payment, import, types

### Community 131 - "Shared Common Package"
Cohesion: 0.67
Nodes (3): ./product, import, types

### Community 132 - "Shared Common Package"
Cohesion: 0.67
Nodes (3): ./storefront, import, types

### Community 133 - "Shared Common Package"
Cohesion: 0.67
Nodes (3): ./utils, import, types

## Knowledge Gaps
- **692 isolated node(s):** `$schema`, `.opencode/plugins/graphify.js`, `$schema`, `AGENTS.md`, `type` (+687 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **77 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `getDb()` connect `Payment Gateways & DTOs` to `Store Management API`, `Store Management API`, `Store Management API`, `Order Management API`, `Product & Catalog API`, `Order Management API`, `Payment Gateways & DTOs`, `Database Schema Definitions`, `Product & Catalog API`, `Product & Catalog API`, `Product & Catalog API`, `Database Schema Definitions`, `Module: Controller`, `Module: Controller`, `Order Management API`, `Product & Catalog API`, `Module: Controller`, `Module: Dto`, `Module: Dto`?**
  _High betweenness centrality (0.076) - this node is a cross-community bridge._
- **Why does `Post` connect `Product & Catalog API` to `Module: Dto`, `Store Management API`, `Store Management API`, `Order Management API`, `Module: Controller`, `Payment Gateways & DTOs`, `Marketing Website Frontend`, `Module: Controller`, `Module: Dto`?**
  _High betweenness centrality (0.042) - this node is a cross-community bridge._
- **Why does `Public()` connect `Store Management API` to `Store Management API`, `Order Management API`, `Order Management API`, `Module: Controller`, `Product & Catalog API`, `Payment Gateways & DTOs`, `Database Schema Definitions`, `Product & Catalog API`?**
  _High betweenness centrality (0.017) - this node is a cross-community bridge._
- **What connects `$schema`, `.opencode/plugins/graphify.js`, `$schema` to the rest of the system?**
  _692 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `Store Management API` be split into smaller, more focused modules?**
  _Cohesion score 0.0522466039707419 - nodes in this community are weakly interconnected._
- **Should `Store Management API` be split into smaller, more focused modules?**
  _Cohesion score 0.05939629990262902 - nodes in this community are weakly interconnected._
- **Should `Storefront UI Components` be split into smaller, more focused modules?**
  _Cohesion score 0.06533646322378717 - nodes in this community are weakly interconnected._