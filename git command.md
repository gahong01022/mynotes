Git 常用指令簡介
🔹 基本設定
git config --global user.name "你的名字"      # 設定使用者名稱
git config --global user.email "你的信箱"     # 設定使用者信箱
🔹 建立與初始化
git init                                       # 初始化 Git 倉庫
git clone <repository-url>                    # 複製遠端倉庫
🔹 狀態與紀錄 回復
git status                                     # 查看當前檔案狀態
git log                                        # 查看提交紀錄
git log --oneline                              # 簡略格式查看提交紀錄
git checkout -- <files>                       # 將文件回復成最新GIT的狀態
🔹 追蹤與提交
git add <檔案>                                 # 加入指定檔案到暫存區
git add .                                      # 加入所有變更
git commit -m "提交訊息"                       # 提交暫存區內容
git commit --amend                           # 更動上一次的commit
🔹 分支操作
git branch                                     # 查看所有分支
git branch <分支名稱>                         # 建立新分支
git branch -av                                # 列出所有分支
git branch -m                                # 重新命名分支名稱
git checkout <分支名稱>                       # 切換分支
git checkout -b <分支名稱>                    # 建立並切換到新分支
git merge <分支名稱>                          # 合併其他分支到當前分支
🔹 遠端操作
git remote -v                                  # 查看遠端倉庫資訊
git remote add origin <url>                   # 新增遠端倉庫
git push origin <分支名稱>                    # 推送本地分支到遠端
git pull origin <分支名稱>                    # 從遠端拉取並合併
git fetch                                     # 拉取遠端更新但不合併
🔹 還原與回溯
git checkout -- <檔案>                         # 還原尚未加入暫存區的變更
git reset <檔案>                               # 取消暫存
git reset --soft                              # 回到最近一次提交，保留取消提挑的內容
git reset --soft   HEAD~2                     # 回到最近2次提交，保留取消提挑的內容
git reset --hard                              # 回到最近一次提交，清除所有變更
git revert <commit-id>                        # 建立反向提交來還原指定提交
git reflog                                    # 查看RESET紀錄
git rebase <branch>                           # 將當的HEAD重設至branch
git merge <branch>                            # 將當前branch合併至當前HEAD
🔹 其他常用
git diff                                       # 查看尚未暫存的變更
git stash                                      # 暫存當前變更
git stash pop                                  # 套用最近一次的暫存
git stash save -u "name"                       # 儲存最近一次的暫存
git stash drop stash@{0}                       # 刪除編號的暫存
git format-patch <commit ID>                   # 把特定commit包成git patch
