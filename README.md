# ios-multi-repo-app
# ios-multi-repo-app
📦 App
 ┣ 📜 AppDelegate.swift
 ┣ 📜 SceneDelegate.swift
 ┗ 📜 AppCoordinator.swift   # Entry point, gọi đến DeepLinkRouter & FeatureFactory

📦 Core
 ┣ 📜 DeepLinkRouter.swift   # Điều hướng đến feature tương ứng
 ┣ 📜 DependencyContainer.swift
 ┗ 📜 FeatureRegistry.swift  # Quản lý danh sách các feature được load

📦 Shared
 ┣ 📜 DeepLinkHandler.swift  # Protocol cho các feature tự implement
 ┣ 📜 DeepLink.swift         # Struct định nghĩa path, params...
 ┣ 📜 Logger.swift
 ┗ 📜 Utilities.swift

📦 Features
 ┣ 📂 LoginFeature
 │  ┣ 📜 LoginFeatureInterface.swift   # Public protocol (expose ra ngoài)
 │  ┣ 📜 LoginFeatureBuilder.swift     # Implement protocol, tạo VC
 │  ┣ 📜 LoginViewController.swift
 │  ┗ 📜 LoginDeepLinkHandler.swift    # Xử lý deep link cho login
 ┣ 📂 ProfileFeature
 │  ┣ 📜 ProfileFeatureInterface.swift
 │  ┣ 📜 ProfileFeatureBuilder.swift
 │  ┣ 📜 ProfileViewController.swift
 │  ┗ 📜 ProfileDeepLinkHandler.swift
 ┗ 📂 SettingsFeature
    ┣ 📜 SettingsFeatureInterface.swift
    ┣ 📜 SettingsFeatureBuilder.swift
    ┗ 📜 SettingsDeepLinkHandler.swift

📦 Resources
 ┣ 📜 Assets.xcassets
 ┗ 📜 Localizable.strings
