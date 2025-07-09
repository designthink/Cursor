# How to Cursor (macOS)

## Get yourself set up
1. Download and install Cursor: https://cursor.com
2. Install recommended extensions:
	- To search and install extensions on Mac press Cmd + Shift + X to open the extensions marketplace, search for the extension, and click install.
	- **Recommended web dev extensions:**
		- **Live Server:** Launches a local development server with live reload
		- **Prettier - Code formatter:** formats your code to make it easier to read
		- **ES7+ React/Redux/React-Native/JS snippets:** React & Next.js shortcuts
		- **Tailwind CSS IntelliSense:** Tailwind CSS autocomplete
		- **ESLint:** Helps find and fix JavaScript problems
		- **GitLens - Git supercharged:** Improves Git integration
		- **Color Highlight:** Displays color chips of hex colors
	- **iOS/macOS extensions & tools:**
		- **[SweetPad](https://github.com/sweetpad-dev/sweetpad) (iOS/Swift development):** Develop Xcode projects and launch simulators
		- **[Swift Language Support](https://marketplace.visualstudio.com/items?itemName=jatindotdev.swift-lsp):** Swift Language Support for Visual Studio Code
		- **Install tools - in Terminal:**
			- Set up [Homebrew](https://brew.sh) if you haven’t already, then install:
				- [xcode-build-server](https://github.com/SolaWing/xcode-build-server): \
						`brew install xcode-build-server`
				- [ios-deploy](https://github.com/ios-control/ios-deploy): \
						`brew install ios-deploy`
				- [xcbeautify](https://github.com/cpisciotta/xcbeautify): \
					`brew install xcbeautify`
				- [swiftformat](https://github.com/nicklockwood/SwiftFormat): \
					`brew install swiftformat`
					
	
## Wondering about tech stacks? Some suggestions:
### Web apps:
- **Frontend:** [Next.js](https://nextjs.org) - React framework for building web apps. Supports server-side rendering (SSR) and static site generation.
- **Backend/Database:** 
	- **Option 1 (all-in-one):** [Supabase](https://supabase.com) – Open-source Firebase alternative with auth, PostgreSQL database, and real-time event support.
	- **Option 2 (advanced):** [FastAPI](https://fastapi.tiangolo.com) – modern, fast, web framework for building APIs with Python. Very high performance, on par with NodeJS and Go.
- **Authentication:** 
	- **Option 1:** [Auth.js](https://authjs.dev) – Flexible open-source authentication library for OAuth and other auth flows. For projects that require a mix of out‑of‑the‑box functionality and custom branding.
	- **Option 2:** [Clerk](https://clerk.com) – Turnkey / plug‑and‑play authentication and user management solution. Designed specifically for modern Next.js applications.
- **Payments:** [Stripe](https://stripe.com/) - Industry-standard gateway for subscriptions and payments.
- **Optional:**
	- [Drizzle ORM](https://github.com/drizzle-team/drizzle-orm): A modern Object-Relational Mapping (ORM) library for JavaScript and TypeScript that provides a simple and type-safe way to interact with databases.*
		- *I haven’t actually used this, but it sounds great.*
- **Cloud ML Models:** [Replicate](https://replicate.com) – lets you run and fine tune ML models via a cloud API, without having to understand the intricacies of machine learning or manage your own infrastructure.
- **Deployment:** [Vercel](https://vercel.com/) – serverless architecture provider for modern web apps. Supports both frontend and server-side processing, including APIs, and automated deployments. Creator of [Next.js](https://nextjs.org)

### Apple only (iOS/iPadOS/macOS):
* Swift + SwiftUI
* Swift [Concurrency](https://developer.apple.com/documentation/swift/concurrency)
* [SwiftData](https://developer.apple.com/xcode/swiftdata/)
* [CloudKit](https://developer.apple.com/icloud/cloudkit/)
* Subscription management (optional): [RevenueCat](https://www.revenuecat.com/docs/getting-started/installation/ios)
 
### Apple+Web:
* Swift + SwiftUI
* Swift [Concurrency](https://developer.apple.com/documentation/swift/concurrency)
* [Alamofire](https://github.com/Alamofire/Alamofire) – Elegant HTTP Networking in Swift
* [Supabase Swift SDK](https://supabase.com/docs/reference/swift/introduction)
* [Supabase Auth](https://supabase.com/docs/reference/swift/auth-api)

### What about other platforms / stacks?:
* **Android:** I’ll let you know if I ever start developing Android apps (one day).
* **React Native:** Never, EVER.
* **Flutter:** People seem to like it. But why bother with a platform that will always be at least one step behind? And when Swift/SwiftUI and Kotlin/Jetpack Compose are so similar to each other? And when AI coding assistants obviate 90% of the need to learn a new language or platform?

## Cursor Rules & Prompts

### [Cursor UI Design Prompt](https://github.com/designthink/Cursor/blob/main/Cursor-UI-Design-Prompt.md)
This is a platform-adaptive UI Design prompt for use in Cursor chat. Use it to creating native-looking user interfaces across different platforms (iPhone, iPad, macOS, and Web).

#### If you just want to try it out:
1. Just paste the entire prompt into chat and hit enter.
2. Then enter a description of your app or feature idea.

#### If you plan to use this prompt regularly:
The best way is to create a "Custom Mode" for Cursor chat:
1. Enable [custom modes](https://docs.cursor.com/chat/custom-modes) in Cursor: `Settings` → `Features` → `Chat` → `Custom modes`
2. Open the mode menu in chat and click `Add custom mode`.
3. Enter a name for the custom mode (e.g. "Generate UI")
4. Set your preferred model (I recommend `claude-4-sonnet`)
5. Optionally create a keyboard shortcut
6. Click on 'Advanced options' and paste in the entire Cursor UI design prompt
7. Make sure 'Generate UI' mode is selected in the chat, and enter a description of your app or feature idea.

