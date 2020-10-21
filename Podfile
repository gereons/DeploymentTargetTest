source 'https://cdn.cocoapods.org/'
use_frameworks! :linkage => :static
inhibit_all_warnings!

install! 'cocoapods', :generate_multiple_pod_projects => true

deployment_target = '13.0'
platform :ios, deployment_target

target 'DeploymentTargetTest' do
    pod 'SDCAlertView'
end

post_install do |installer|
    installer.generated_projects.each do |project|
        project.targets.each do |target|
            target.build_configurations.each do |config|
                config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = deployment_target
            end
        end
    end
end
