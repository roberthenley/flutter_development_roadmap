by [Robert Henley](https://www.linkedin.com/in/robertallenhenley/)

After completing the [Complete 2020 Flutter Development Bookcamp](https://www.udemy.com/course/flutter-bootcamp-with-dart/) from [The App Brewery](https://www.appbrewery.co/), I found myself lost. There was a lot of Flutter documentation, videos, and other resources. I was not sure where to go next. I was one of a couple of people to raise this issue at the FlutterLDN/Flutter Berlin joint meetup in May 2020, but no one had an answer.

Serendipity struck that night when I found Oleksandr Leuschenko's (@olexale) [Highly Subjective Roadmap to Flutter Development](https://github.com/olexale/flutter_roadmap) on [Awesome Flutter](https://github.com/Solido/awesome-flutter). That roadmap let me assess where I was on my journey toward professional Flutter development.

I recommend you have a look at that roadmap; it's a beautiful infographic and the page has a lot of useful links.  

Over time, I found that I had my own ideas about the topic. So here is my version of a Flutter development roadmap. It is more detailed than the original, and at least as subjective. Please note that there is no one true path to learn Flutter, and I'm not following this roadmap in linear order myself -- I've skipped around it as various courses and activities filled in gaps. But it serves to keep me oriented as I progress, knowing what I know and what I've yet to learn. I hope it can help you find your own way.

If you want to track your progress, I've created a [Flutter Development Study Checklist](https://docs.google.com/spreadsheets/d/1guOBy3n8n1-b8ro-xF3OfO-fn-oJGTaZlf0lC6_176w/edit?usp=sharing). This spreadsheet allows you to check off study topics and to rate your level of knowledge in each topic. Use `File > Make a copy` to fill in your progress.


## Getting Started

* **Flutter: What and Why?** (required)
  * High-level overview
  * Flutter's architecture
  * Walk through starter app code
  * Why Dart?

  Every course and book on Flutter covers this to a greater or lesser extent. 


* **Development Environment**
  * Android Studio or Visual Studio Code (required)
  * Flutter Command Line Interface (CLI) (installation required; knowledge of use helpful)
  * XCode and iOS emulator (required for iOS development; otherwise, optional, and only possible if you have a Mac)
  * Git (helpful)
  * DartPad (optional)

  The [App Brewery course](https://www.udemy.com/course/flutter-bootcamp-with-dart/) covers development environment setup well, including iOS, but not including git. They show how to get starting by pulling projects from Github, but not the important source code control issues like branching, committing, pull requests, and merging. Seek that knowledge elsewhere, because it will be required in a professional job -- and even on your side projects, knowing you have the safety of saved code versions helps.

  [DartPad](https://dartpad.dev/) is also a useful tool to know about. Whether you use it or not depends on your needs, but most video courses will introduce you to it when demonstrating Dart language concepts.


* **The Dart Language**
  * Dart basics: expressions, data types, identifiers and assignment, conditionals, basic looping. (required)
  * Objects: classes, properties, constructors, methods, and simple inheritance (required)
  * Functions: function declarations, positional parameters, named parameters, return values, callbacks (required)
  * Null safety (eventually required)
  * Code style (required)
  * Static analysis and linters, e.g. [extra\_pedantic](https://pub.dev/packages/extra_pedantic) package (eventually required)
  * Essential Dart Libraries: dart:core and dart:math (eventually required)

  This is the level of Dart knowledge that you'll get from a chapter in a Flutter introductory book, and it's all you'll need to get going. The [App Brewery course](https://www.udemy.com/course/flutter-bootcamp-with-dart/) introduces Dart language feature as they are needed for the sample applications being constructed and it will take you to the minimum level necessary. So would [_Flutter in Action_](https://www.manning.com/books/flutter-in-action).
  
  Null safety in Dart is newer, but it is available in Flutter 2 as of March 3, 2021, and it is _essential_ to learn it; although, it's not taught in the introductory books or video courses as of this writing. See [Null safety in Flutter](https://flutter.dev/docs/null-safety).
  
  The [Effective Dart](https://dart.dev/guides/language/effective-dart) section of the Flutter docs is your best resource about coding style. The IDEs will also help you adopt common coding conventions with warnings. You can enhance those warnings greatly with static analysis packages like [extra\_pedantic](https://pub.dev/packages/extra_pedantic).

  You also need to know some basic Dart library methods. But you don't yet need to know deep Object-Oriented Programming or Functional Programming practices at this stage -- they will come along later.

There will be more Dart to learn later, but you're now ready to learn Flutter.

## Basic Flutter

* **Basic Widgets**
  * Material Widgets (required)
  * Stateful vs. Stateless widgets (required)
  * Basic Material Design (required)
  * Application assets (required)
  * Fonts (helpful)
  * Cupertino Widgets (helpful)
  * [Material Design](https://material.io/design) and [Apple Mobile Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/) (eventually required)

  Flutter is all about widgets. The most used widgets in one survey were: [Text](https://api.flutter.dev/flutter/widgets/Text-class.html), [Container](https://api.flutter.dev/flutter/widgets/Container-class.html), [Padding](https://api.flutter.dev/flutter/widgets/Padding-class.html), [Column](https://api.flutter.dev/flutter/widgets/Column-class.html), [Icon](https://api.flutter.dev/flutter/widgets/Icon-class.html), [Row](https://api.flutter.dev/flutter/widgets/Row-class.html), [SizedBox](https://api.flutter.dev/flutter/widgets/SizedBox-class.html), [Center](https://api.flutter.dev/flutter/widgets/Center-class.html), [Expanded](https://api.flutter.dev/flutter/widgets/Expanded-class.html), and [Scaffold](https://api.flutter.dev/flutter/material/Scaffold-class.html). Those, plus [StatelessWidget](https://api.flutter.dev/flutter/widgets/StatelessWidget-class.html), [StatefulWidget](https://api.flutter.dev/flutter/widgets/StatefulWidget-class.html), and [MaterialApp](https://api.flutter.dev/flutter/material/MaterialApp-class.html) are a bare minimum. 
  
  Learning the Icon widget also means you need to know about app assets, and font handling for Text is helpful. 
  
  The [App Brewery class](https://www.udemy.com/course/flutter-bootcamp-with-dart/) covers those and more; it even gives an introduction to the Cupertino widgets. But to learn many more widgets, watch the [Widget of the Week](https://bit.ly/2Njce4W) videos from the Flutter team and explore [Material Design](https://material.io/design).
  
  
* **Basic Package Management**
  * Pub and [pub.dev](https://pub.dev/) (required)
  * pubspec.yaml (required)
  * Popular libraries and plug-ins (helpful)

  Knowing how to find libraries and plug-ins on [pub.dev](https://pub.dev) and install them in your applications is essential. Knowing what packages are popular and fit your apps' needs will come over time: the "Package of the Week" videos on the Flutter YouTube channel can help. Some packages for specific needs are suggested below.


* **Basic Application Architecture -- State Management**
  * Local State via StatefulWidget vs. Shared state (required)
  * Lifting State Up pattern (required)
  * Provider package (required)

  The [App Brewery full course](https://www.udemy.com/course/flutter-bootcamp-with-dart/) has you covered here. See also the video ["Pragmatic State Management in Flutter"](https://www.youtube.com/watch?v=d_m5csmrf7I) from Google I/O 2019. Alternative state management approaches are discussed below, because they take a more holistic view of application architecture.


* **Multi-Page Applications**
  * Routing 1.0 (required)
  * Routing 2.0 and wrappers like the [flow\_builder](https://pub.dev/packages/flow_builder) package (helpful -- required in some cases)
  * Code generation-based routing, e.g. the [auto\_route](https://pub.dev/packages/auto_route) package (helpful)
  * Hero animations (helpful)

  Moving beyond a single page is a key step in application organization. The [App Brewery course](https://www.udemy.com/course/flutter-bootcamp-with-dart/) covers the Routing 1.0 methods, but not Routing 2.0, which is newer and more complex. Look into the Routing 2.0 wrapper packages that are emerging, like [flow\_builder](https://pub.dev/packages/flow_builder), or code-generating alternatives like [auto\_route](https://pub.dev/packages/auto_route). And [Hero animations](https://flutter.dev/docs/development/ui/animations/hero-animations) are a useful page transition technique.

By this point, you can create basic Flutter applications. Now move on to learn the tools for creating more sophisticated applications.

## Mid-Level Flutter

* **Networking**
  * Asynchronous Dart programming: Future, async/await (required)
  * HTTP client-server concepts and the [http](https://pub.dev/packages/http) package (required)
  * JSON parsing and serialization: the [dart:convert](https://api.dart.dev/stable/2.10.5/dart-convert/dart-convert-library.html) library (required)
  * RESTful API concepts (helpful)
  * Advanced http packages: [dio](https://pub.dev/packages/dio) (helpful)
  * Code-generation-based packages for networking: [retrofit for Dart](https://pub.dev/packages/retrofit) (uses [dio](https://pub.dev/packages/dio) and [json\_serializable](https://pub.dev/packages/json_serializable)) (helpful) 
  * [GraphQL](https://graphql.org/) concepts and the [graphql_flutter](https://pub.dev/packages/graphql_flutter) package (optional)

  The [App Brewery course](https://www.udemy.com/course/flutter-bootcamp-with-dart/) (and most books) covers the must-haves for networking. As you go deeper, you'll want to understand how [Representational State Transfer (REST)](https://en.wikipedia.org/wiki/Representational_state_transfer) works, more advanced networking (like interceptors and transformers), and how to handle code-generation-based packages. Later, you can learn how [GraphQL](https://graphql.org/) provides an alternative to REST.


* **Intermediate User Interfaces**
  * [How the layout process works for all widgets](https://flutter.dev/docs/development/ui/layout/constraints) (required)
  * Displaying lists: [Dart Streams](https://api.dart.dev/stable/2.10.5/dart-async/Stream-class.html), [StreamBuilder](https://api.flutter.dev/flutter/widgets/StreamBuilder-class.html), and [ListView](https://api.flutter.dev/flutter/widgets/ListView-class.html) (required)
  * Responsive UI: Change layout by display size
      * [MediaQueryData](https://api.flutter.dev/flutter/widgets/MediaQueryData-class.html) display parameters (required)
      * [LayoutBuilder](https://api.flutter.dev/flutter/widgets/LayoutBuilder-class.html) (required)
      * [responsive\_builder](https://pub.dev/packages/responsive_builder) or [responsive\_framework](https://pub.dev/packages/responsive_framework) (helpful)
  * Adaptive UI: Show Material widgets on Android and Cupertino widgets on iOS
      * [flutter\_platform\_widgets](https://pub.dev/packages/flutter_platform_widgets) (helpful)
  * Animations
      * Implicit animations (required)
      * Transition animations (required)
      * Explicit animations (helpful)
      * Staggered animations (helpful)
      * Animation accessibility: when, how, and why not to animate (helpful)
      * [Lottie](https://pub.dev/packages/lottie) (optional)
      * [Rive](https://rive.app/) (optional)

  Learning how the layout process actually works is critical, and the [Understanding Constraints](https://flutter.dev/docs/development/ui/layout/constraints) documentation covers it best.
  
  Most user interfaces also need lists, which are driven by [Dart Streams](https://api.dart.dev/stable/2.10.5/dart-async/Stream-class.html), [StreamBuilder](https://api.flutter.dev/flutter/widgets/StreamBuilder-class.html), and [ListView](https://api.flutter.dev/flutter/widgets/ListView-class.html). Most books and courses cover this.
  
  More professional apps should also adapt to the display they run onto and probably should adapt to the platform as well. But you won't find much about this in introductory courses or books. At least learn about [MediaQueryData](https://api.flutter.dev/flutter/widgets/MediaQueryData-class.html).
  
  [Animations](https://flutter.dev/docs/development/ui/animations) are also helpful for some applications -- and you need to know how MediaQueryData.disableAnimations tells your app not to animate, as well as [how flashing, blinking, and parallax motion can harm users](https://www.smashingmagazine.com/2018/04/designing-accessibility-inclusion/#lens-animation-effects). Most Flutter books and video courses cover animation, except animation accessibility.
  
  
* **Simple Persistence**
  * Serializers: [dart:convert](https://api.dart.dev/stable/2.10.5/dart-convert/dart-convert-library.html) library for non-JSON data (required)
  * Files: [path\_provider](https://pub.dev/packages/path_provider) and dart:io (required)
  * Local storage: the [localstorage](https://pub.dev/packages/localstorage) plugin (required)
  * Code-generation-based serialization: the [built\_value](https://pub.dev/packages/built_value) package (helpful)
  * Keychain and Keystore: the [flutter\_keychain](https://pub.dev/packages/flutter_keychain) package (optional)

  When you just need to store simple data, use the simplest storage solution possible.


* **Authentication**
  * Firebase Auth and [firebase\_auth](https://pub.dev/packages/firebase_auth) package (required)
  * Google Sign In and [google\_sign\_in](https://pub.dev/packages/google_sign_in) package (helpful)
  * Sign In with Apple (eventually required)
  * Facebook sign in (optional)
  * Local market authentication providers (optional, but critical in some markets)

  Most apps have some sort of sign-in system: some based on id and password, others based on more complex server interactions. Mostly, Firebase Auth has your back here, and the [App Brewery course](https://www.udemy.com/course/flutter-bootcamp-with-dart/) covers it lightly, but in some cases you want more specific forms of authentication. Look for appropriate packages on [pub.dev](https://pub.dev). Know your user base: some less-obvious authentication providers are necessary in local markets, such as LINE Login in Japan ([flutter\_line\_login](https://pub.dev/packages/flutter_line_login)). Also, Sign In with Apple is required for iOS apps that use other social login systems.


* **Database**
  * Firebase Firestore (required)
  * Relational databases: SQLite with [sqflite](https://pub.dev/packages/sqflite) package (required)
  * NoSQL databases: [hive](https://pub.dev/packages/hive) package (helpful)
  * [Moor](https://pub.dev/packages/moor) (optional)

  When your data storage requirements are larger, more complex, or more structured, use a database. The [App Brewery course](https://www.udemy.com/course/flutter-bootcamp-with-dart/) covers Firebase Firestore, which is a service, but client-local databases are also available.


* **Application Architecture -- Seperation of Concerns**
  * Business Logic Component (BLoC) pattern and [flutter\_bloc](https://pub.dev/packages/flutter_bloc) package (required)
  * Dependency Injection: [get\_it](https://pub.dev/packages/get_it) and [injectable](https://pub.dev/packages/injectable) packages (required)
  * Immutability and Unidirectional Data Flow: the [freezed](https://pub.dev/packages/freezed) package (helpful)
  * Design Patterns and Clean Architecture (helpful)
  * [Riverpod](https://pub.dev/packages/riverpod) package (helpful)
  * [Redux](https://pub.dev/packages/redux) (optional)
  * [MobX](https://pub.dev/packages/mobx) (optional)
  * MV* architecture patterns: MVC, MVP, MVVM, etc. (optional)

  This is where apps start to get serious: these techniques separate larger apps into maintainable pieces. This is also the point where the ideas from books like [_Design Patterns_](https://www.pearson.com/us/higher-education/program/Gamma-Design-Patterns-Elements-of-Reusable-Object-Oriented-Software/PGM14333.html) and [_Clean Code_](https://www.pearson.com/us/higher-education/program/Martin-Clean-Code-A-Handbook-of-Agile-Software-Craftsmanship/PGM63937.html) / [_Clean Architecture_](https://www.pearson.com/us/higher-education/program/Martin-Clean-Architecture-A-Craftsman-s-Guide-to-Software-Structure-and-Design/PGM333762.html) begin to come into play. You won't find this in introductory courses. Some of these topics are covered by [@resocoder's YouTube videos](https://www.youtube.com/c/ResoCoder). 
  
  The BloC pattern is recommended by Google, especially in conjunction with the [Provider](https://pub.dev/packages/provider) state management package. (I liked WKCD's video series [BLoC - from zero to HERO](https://www.youtube.com/watch?v=w6XWjpBK4W8&list=PLptHs0ZDJKt_T-oNj_6Q98v-tBnVf-S_o&index=2) for training.) 
  
  An alternative to using Provider is the [Riverpod](https://pub.dev/packages/riverpod) package from the same author, which was designed to address Provider's defects (such as type safety); it is considered an experiment, but I've heard good reports about it.
  
 [Redux](https://pub.dev/packages/redux) and [MobX](https://pub.dev/packages/mobx) come out of the React web community and remain popular and powerful, so although using them is optional, it's good to know what they are and what they can do. Ditto the MV* architectures: while they are less used in Flutter, people talk about them often as points of comparison.


* **Testing**
  * Unit Testing (required)
  * Mock Objects and the [mockito](https://pub.dev/packages/mockito) package (required)
  * Widget Testing (required)
  * On-device testing with [flutter\_driver](https://api.flutter.dev/flutter/flutter_driver/flutter_driver-library.html) (required)
  * [Integration testing](https://flutter.dev/docs/cookbook/testing/integration/introduction) with [integration\_test](https://pub.dev/packages/integration_test) package (required)
  * Behavior-Driven Development (BDD) and the [gherkin](https://pub.dev/packages/gherkin) package (for Dart), and/or the [bdd\_widget\_test](https://pub.dev/packages/bdd_widget_test) or [flutter\_gherkin](https://pub.dev/packages/flutter_gherkin) packages (for Flutter) (helpful)
  *	 Test-Driven Development (TDD) (helpful)

  The subject of testing is critical, and could easily be introduced earlier in training -- right after basic Dart, in fact. But that's not how most courses are structured, and it does help to have architectural patterns that seperate concerns in place first, because they make the app more testable. [_Flutter in Action_](https://www.manning.com/books/flutter-in-action) covers testing somewhat. The integration\_test package is new; see [Updates on Flutter Testing](https://medium.com/flutter/updates-on-flutter-testing-f54aa9f74c7e).

You can now build complex Flutters applications, but not quite professional-grade ones.

## Industrial-Grade Flutter

* **Advanced User Interfaces**
  * The widget lifecycle (required)
  * Element Tree and RenderObject (required)
  * [Internationalization and Localization](https://flutter.dev/docs/development/accessibility-and-localization/internationalization)
      * flutter\_localization, \*App.localizationDelegates and .supportedLocales (required)
      * [Intl](https://pub.dev/packages/intl) package (required)
      * [easy\_localization](https://pub.dev/packages/easy_localization) (helpful)
      * Localization services and automation (optional)
  * [Accessibility](https://flutter.dev/docs/development/accessibility-and-localization/accessibility): Allow assistive technologies like TalkBack and VoiceOver or an external keyboard/switch device to present and operate your app to people with disabilities
      * semanticLabel and excludeFromSemantics attributes (required)
      * [Semantics](https://api.flutter.dev/flutter/widgets/Semantics-class.html) widget (required)
      * [SemanticsService.announce()](https://api.flutter.dev/flutter/semantics/SemanticsService/announce.html) (required)
      * [MediaQueryData](https://api.flutter.dev/flutter/widgets/MediaQueryData-class.html) accessibility flags (eventually required)
      * Android [Accessibility Scanner](https://developer.android.com/guide/topics/ui/accessibility/testing#accessibility-scanner) and iOS [Accessibility Inspector](https://developer.apple.com/library/archive/documentation/Accessibility/Conceptual/AccessibilityMacOSX/OSXAXTestingApps.html) (helpful)
      * Manual accessibility testing (helpful)
  * Custom Painting (helpful)

  There's a lot more than widgets to a complex user interface. [_Flutter in Action_](https://www.manning.com/books/flutter-in-action) covers the widget lifecycle, the Render tree, accessibility, and custom painting. 
  
  Internationalization is covered in the [Flutter docs](https://flutter.dev/docs/development/accessibility-and-localization/internationalization). 
  
  Digital accessibility for the disabled is a large topic in itself, but it's both the right thing to do and a legal requirement for apps in major markets. Accessibility is most often taught for the web; start with this [W3C introductory course](https://www.edx.org/course/web-accessibility-introduction) for background, then apply what you've learned using these [Flutter docs](https://flutter.dev/docs/development/accessibility-and-localization/accessibility). This list of [accessibility guideline suggestions](https://theappbusiness.github.io/accessibility-guidelines/) may help, as it includes guidance for Flutter, but it's incomplete.


* **Advanced Dart**
  * Dart Isolates (required)
  * Modules and Libraries (helpful)
  * Intermediate to advanced Object-Oriented Programming (OOP) (helpful)
  * More Design Patterns and Design Principles: [Gang of Four](https://en.wikipedia.org/wiki/Design_Patterns), [SOLID](https://en.wikipedia.org/wiki/SOLID), [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself), ... (helpful)
  * Functional Programming (FP) (optional)

  Dart Isolates allow true parallel execution of code, which is great for large computations. Knowing how Dart code can be modularized and placed in independent libraries will help simplify larger projects. More advanced OOP, Design Patterns, and Design Principles become relevant at this level of complexity: look especially at [SOLID](https://en.wikipedia.org/wiki/SOLID) to be sure your class hierarchies make sense and [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself) to make sure your methods are small and well-structured. With Functional Programming, the discipline of using only immutable objects is elevated to high art with the introduction of higher-order functions, which are genuine power tools of abstract coding.


* **Performance Profiling**
  * Memory Leaks (required)
  * DevTools (required)
  * App Size (helpful)
  * CPU load and Jank (helpful)

  Sooner or later the size or speed of your app will not be what users need. Profiling tools will help you find out why and fix it. See the [Flutter Performance Docs](https://flutter.dev/docs/perf). See also Filip Hráček's [Performance Testing of Flutter Apps](https://medium.com/flutter/performance-testing-of-flutter-apps-df7669bb7df7) article and [Performance: Optimizing Your Flutter App](https://www.youtube.com/watch?v=SQcmrl_NkqY) video.

* **Flutter Web** (optional)
  * Basic HTML and JavaScript knowledge (required for this option)
  * See [https://flutter.dev/web](https://flutter.dev/web) for setup
  * Use only web-enabled [pub.dev](https://pub.dev) packages

  Flutter web development is not greatly different from Flutter mobile app development. You will need to place a greater emphasis on responsive layouts, because web form factors differ more than pure mobile apps. Web development is actually an option from the beginning of your development journey, but there are limitations to Flutter web (e.g., no hot reload) and the relative immaturity of the technology that make me categorize it as an advanced topic.

* **Flutter Desktop** (optional -- in Beta)
  * See [https://flutter.dev/desktop](https://flutter.dev/desktop) for details
  * Desktop platform development tools, e.g. Visual Studio for Windows, XCode for Mac, and various command line tools for Linux (required for this option)
  * Use only [pub.dev](https://pub.dev) packages enabled for the selected desktop platform(s)
  * Learn appropriate platform UI guidelines and accessibility standards

  Flutter can also be used to create desktop native applications for Windows, Mac, and Linux. This is Beta-quality software, but available for you to play with. YMMV.

* **Plug-ins** (eventually required)
  * Native Platform APIs:
      * iOS and Swift
      * Android and Kotlin
      * Web and HTML, CSS, and JavaScript
      * Desktop OS APIs (optional)
  * Platform Channels
  * Dart Foreign Function Interface (FFI) and the [ffi](https://pub.dev/packages/ffi) package
  * Creating and publishing libraries and plug-ins on pub.dev

  You have already encountered packages and the [pub.dev](https://pub.dev) site. Learning how to create your own packages is valuable for large projects. And it's likely that someday you're going to have to debug a plug-in your app uses or write your own; at which point, you're going to need to know how to deal with the underlying native platform, its language(s) and API. Platform Channels and Dart FFI are two ways to tie your Dart and Flutter code to that native code.


* **Flutter Internals (optional)**
  * Framework Architecture
  * Rendering Engine in-depth
  * Dart VM

  It's nice to know the underlying mechanisms of your framework, but you can be a very effective Flutter developer without it. Just be prepared to dive in and understand how things _really_ work when you have to. 

By this point, you know enough to build professional-grade applications with Flutter. But that doesn't get your app into people's hands.

## End-Game

* **Continuous Integration**
  * CI servers/services: Codemagic, Bitrise, Travis, GitHub Actions, Circle CI, etc. Pick one. (required)
  * Test Build Distribution: Microsoft AppCenter, TestFlight, Google Play Store Alpha, etc. (required)
  * FastLane (helpful)
  * Code metrics (optional)

  Automated builds based on your source code control system are a must! You'll also need a way to distribute test builds to manual testers, and ways to measure your code base health (e.g., test code coverage, static code analysis). This is "Flutter Ops" and you need to know about it.


* **Analytics (required)**
  * Usage Analytics
  * Crash Logging
  * A/B Testing

  Always measure your apps or you'll be just guessing who your users are and what they do with your app. Firebase Analytics is one tool for that. Especially, get crash reports from the field, because you can't find edge cases nearly as well as a lot of users can. A/B testing lets you figure out which alternative designs work better for people.


* **Stores (required)**
  * [AppStore Guidelines](https://developer.apple.com/app-store/guidelines/)
  * [Google Play Store Guidelines](https://play.google.com/about/developer-content-policy/)
  * App Store Connect
  * Google Dev Console

  The stores are the final end-game: where you want your app to go. But can it? There are rules, and it's on you to know them. Plus, you have to know how to actually push the button to publish and what happens next.

## The End (of the Beginning)

Congratulations! You can now go deeper on anything above. Learning Flutter is an iterative process -- there is more to learn in any category, and likely categories you will discover that I haven't thought of. Also, new widgets, packages, and plug-ins are constantly being created, and you'll want to keep learning them. Have fun!


A Flutter Development Roadmap by [Robert Henley](https://www.linkedin.com/in/robertallenhenley/) is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/?ref=chooser-v1) <img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" alt="" /><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" alt="" />