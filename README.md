# wrobot(只支持windows系统,linux另有项目)

## 本项目只是提供代码，不对使用者因使用本代码实际产生的盈亏负责，毕竟赚了钱也没分给我，亏了钱也只能自己扛

## 提供多级动态止盈就是所谓的追踪止盈、回撤止盈，提供6级，需要自行计算止盈的数值

# 注意

## API的权限只需要有交易权限就够了，不要开提币权限！

## API的权限只需要有交易权限就够了，不要开提币权限！

## API的权限只需要有交易权限就够了，不要开提币权限！

# 使用说明

下载本项目代码压缩包，放在C盘根目录下，解压，最终代码在C:\wrobot\下。如果是git下载，也请代码放在C:\wrobot\下，建议使用git下载，方便后续更新

安装相关库(只支持python3)  pip3 install -r requirements.txt 或 pip install -r requirements.txt

安装postgresql,这个自行搜索安装。注意要记录数据库登录密码，然后还要建一个数据库，记录好数据库名，一会安装要用

安装redis，启动

到这，准备工作做好。在项目目录C:\wrobot\下执行python3 install.py  然后在浏览器打开http://127.0.0.1:5001/ 

根据浏览器上边的提示进行配置就行。

安装好，关掉运行，如果不关掉可以打开一个新的cmd命令窗口。然后就是在项目目录C:\wrobot\下执行python3 run_admin.py  然后在浏览器打开http://127.0.0.1:5002/

浏览器打开http://127.0.0.1:5002/ 会看到登录界面，输入刚才配置的登录信息。

登录后看到三个菜单：主页(相关日志)，自动交易(设置交易对及相关配置)，我的帐户(修改系统密码及配置交易所API信息)。目前只支持OKEX交易所，需要自己去OKEX申请API相关的密钥信息。

在我的帐户输入交易所信息，然后在自动交易进行添加交易对及配置。配置好还要运行任务及机器人。

运行任务：重新打开一个cmd在项目目录C:\wrobot\下执行python3 run_task.py

运行机器人：重新打开一个cmd在项目目录C:\wrobot\下执行python3 run_robot.py

到此，所有都运行好了。不用管，相关持仓及订单信息请看OKEX的网页或者APP对应的交易对下的数据。

如果后续有更新代码，可以直接git下载就好了。下载好后，关掉cdm窗口，重新打开窗口执行python3 run_admin.py，python3 run_task.py，python3 run_robot.py就好了，注意要在项目目录下运行哦。

如在使用过程中，有问题请联系下方QQ

如果需要外网访问，可以自己配置nginx进行代理，这样就方便很多，不会的请自行搜索。

##关于代码更新说明
建议使用git命令来下载，这样更新就不影响。如果下载压缩包的方法，那么要注意保存安装后的dbconfig.py这个文件。安装成功一次是有dbconfig.py这个文件，如果下载压缩包，直接将这个文件放到解压出来的目录下就不用重复安装，直接运行就可以了，之前的配置及相关数据不受影响。

## 自定义配置

custom/features.py 这个文件提供使用自己的策略，提供了止盈止损的处理等，可以自行研究，如有问题请联系我进行修正。

## 多级动态止盈配置说明

由于不同的币(交易标的)，不同的交易张数，不同的行情所产生的收益是不一致的，这就要求在配置多级动态止盈时所填写的收益值及回撤值需要自己计算。
由于我也没有确定相关收益值及回撤值，所以是没有任何参考数据的，需要使用者自己小额使用，再根据持仓日志，止盈止损日志，持仓流水三个页面的记录数据，自己计算出不同的收益值，
在达到某个回撤值时进行止盈。页面及代码都有计算说明，目前我也是用ETH永续本币，每次交易１张，准备根据相关日志来确定不同的收益值要设置多少的回撤值。当我确定了我的收益值及回撤值会在些提示参考。

# 更新日志  (开源协议为MIT)

2020-09-23  增加多级动态止盈未达要求时的文字说明，增加持仓流水对说明内容的搜索，止盈止损日志增加系统订单号，方便后续计算具体的止盈收益值与回撤值要用数据做具体的参考数值。更正多级动态止盈计算公式。

2020-09-22  初始始上传


# 联系

QQ173782910
