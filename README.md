#Zech
# devops-netology
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

