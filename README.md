# toolbox

exp : find . -iname *.[ch] -exec grep --color -wn -H "$*" {} \;

类似命令脚本可以使用 find . -name "*" |xargs grep str 此命令没有颜色亮色区分

exp脚本用于从需要检索的文件中检索特定的字符串，默认添加了检索.h .cpp .php文件，如需要检索其他文件类型可自行添加。
