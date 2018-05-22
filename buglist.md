更新方法（以更新到react-native0.55.4为例）
ls -A | grep -vE '^(\.git|buglist\.md)$' | xargs rm -rf
wget http://registry.npm.taobao.org/react-native/download/react-native-0.55.4.tgz
tar -xf react-native-*.tgz
cp -r package/. .
rm -rf package react-native-*.tgz
根据bug列表和git历史在新的版本上进行修改
提交到github，修改项目依赖的提交版本

bug列表
[iOS][TextInput] Fix controlled TextInput for Chinese (and other languages)
https://github.com/facebook/react-native/pull/18456/files
修复方法：pull request
