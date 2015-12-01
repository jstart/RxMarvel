# Uncomment this line to define a global platform for your project
# platform :ios, '6.0'

use_frameworks!
inhibit_all_warnings!

target 'FunctionalMarvel' do
pod 'RxAlamofire', '= 0.3.3'
pod 'Argo'
pod 'RxSwift', '= 2.0.0-beta.3'
pod 'RxCocoa', '= 2.0.0-beta.3'
pod 'Curry'
pod 'Runes'
pod 'SDWebImage'
end

target 'FunctionalMarvelTests' do

pod 'Quick'
pod 'Nimble'
pod 'RxAlamofire', '= 0.3.3'
pod 'Argo'
pod 'RxSwift', '= 2.0.0-beta.3'
pod 'RxCocoa', '= 2.0.0-beta.3'
pod 'Curry'
pod 'Runes'

end

post_install do |installer|
   installer.pods_project.targets.each do |target|
      if target.name == 'RxSwift'
         target.build_configurations.each do |config|
            if config.name == 'Debug'
               config.build_settings['OTHER_SWIFT_FLAGS'] ||= ['-D', 'TRACE_RESOURCES']
            end
         end
      end
   end
end
