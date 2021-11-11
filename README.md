#Zech
# devops-netology
1.git show aefea
aefead2207ef7e2aa5dc81a34aedf0cad4c32545
Update CHANGELOG.md
2.tag: v0.12.23
3. git show b8d720  итого 2 родителя
git show 56cd7859e
git show 9ea88f22f
56cd7859e05c36c06b56d013b55a252d0bb7e158
9ea88f22fc6269854151c571162c5bcf958bee2b
4. git log v0.12.23..v0.12.24 --oneline
33ff1c03b (tag: v0.12.24) v0.12.24
b14b74c49 [Website] vmc provider links
3f235065b Update CHANGELOG.md
6ae64e247 registry: Fix panic when server is unreachable
5c619ca1b website: Remove links to the getting started guide's old location
06275647e Update CHANGELOG.md
d5f9411f5 command: Fix bug when using terraform login on Windows
4b6d06cc5 Update CHANGELOG.md
dd01a3507 Update CHANGELOG.md
225466bc3 Cleanup after v0.12.23 release
5. git log -S'func providerSource' --oneline
8c928e835 main: Consult local directories as potential mirrors of providers
git show 8c928e835 
6.git show 
git grep globalPluginDirs
git grep "func globalPluginDirs"
git log -L :globalPluginDirs:plugins.go --oneline
78b122055 Remove config.go and update things using its aliases
52dbf9483 keep .terraform.d/plugins for discovery
41ab0aef7 Add missing OS_ARCH dir to global plugin paths
7. git log -S'synchronizedWriters' --pretty
Author: Martin Atkins <mart@degeneration.co.uk>




#
**/.terraform/* Будут проигнорированы файлы с названием .terraform во всех дирректориях и все файлы, в поддиректориях найденного файла


# .tfstate files не исполняется
*.tfstate Будут проигнорированы файлы с расширением в текущей дирректории
*.tfstate.* будут проигнорированы файлы, имеющие в названии .tfstate.

# Crash log files
crash.log Будет проигнорирован файл с этим названием в текущей дирректории

# Exclude all .tfvars files, which are likely to contain sentitive data, such as
# password, private keys, and other secrets. These should not be part of version
# control as they are data points which are potentially sensitive and subject
# to change depending on the environment.
#
*.tfvars Будут проигнорированы файлы с расширением в текущей дирректории

# Ignore override files as they are usually used to override resources locally and so
# are not checked in
override.tf Будет проигнорирован файл с этим названиемв текущей дирректории
override.tf.json Будет проигнорирован файл с этим названиемв текущей дирректории
*_override.tf Будут проигнорированы файлы окончанием в названии _override.tf в текущей дирректории
*_override.tf.json Будут проигнорированы файлы окончанием в названии _override.tf.json в текущей дирректории

# Include override files you do wish to add to version control using negated pattern
#
# !example_override.tf

# Include tfplan files to ignore the plan output of command: terraform plan -out=tfplan
# example: *tfplan*

# Ignore CLI configuration files
.terraformrc Будут проигнорированы файлы с .terraformrc названием в текущей дирректории
terraform.rc Будет проигнорирован файл с этим названием в текущей дирректории

