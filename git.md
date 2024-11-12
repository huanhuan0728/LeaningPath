<img width="816" alt="image" src="https://github.com/user-attachments/assets/31b854a4-6919-43e1-936b-aae81aa9ea72">

# vscode运行c代码
## 1. `gcc sorting_algorithms.c main.c -o sorting_demo`

这是一个编译命令，使用 `gcc`（GNU Compiler Collection）编译 C 程序：

- **`gcc`**：调用 GNU C 编译器，将源代码编译为可执行文件。
- **`sorting_algorithms.c main.c`**：指定要编译的源文件。这里包含了两个文件：
  - `sorting_algorithms.c`：包含排序算法的实现。
  - `main.c`：包含 `main` 函数，通常是程序的入口点，调用排序函数来测试排序算法。
- **`-o sorting_demo`**：指定输出文件的名称。`-o` 是 `output` 的缩写，表示编译后的可执行文件名称。
  - 在这里，生成的可执行文件名为 `sorting_demo`。如果不加 `-o` 选项，编译器会默认生成一个名为 `a.out` 的可执行文件。

完整意思是：将 `sorting_algorithms.c` 和 `main.c` 编译为一个名为 `sorting_demo` 的可执行文件。

## 2. `./sorting_demo`

这是运行生成的可执行文件的命令：

- **`./`**：表示当前目录。直接运行可执行文件时需要在文件名前加 `./`，因为系统通常不会自动在当前目录中查找可执行文件。`./` 告诉终端去当前目录寻找文件。
- **`sorting_demo`**：可执行文件的名称，即上一步编译生成的文件。

完整意思是：在当前目录中运行 `sorting_demo` 可执行文件。

## 总结

这两条命令的作用是：
1. 使用 `gcc` 将 `sorting_algorithms.c` 和 `main.c` 编译成一个名为 `sorting_demo` 的可执行文件。
2. 运行该 `sorting_demo` 可执行文件，执行程序的逻辑。

# git
## 通过以下步骤将 GitHub 上的项目拉取到本地：

1. **复制 GitHub 仓库的 URL**：
   - 打开你想要拉取的 GitHub 仓库页面。
   - 点击页面上方的绿色按钮 **Code**，然后选择 **HTTPS** 或 **SSH**，并复制仓库的 URL。

2. **打开终端**：
   - 在你的 Mac 上打开终端（Terminal）。

3. **克隆仓库到本地**：
   - 在终端中，导航到你想要保存项目的文件夹，输入以下命令，并将 `仓库的URL` 替换为你刚才复制的 URL：
     ```bash
     git clone 仓库的URL
     ```
   - 例如，如果仓库的 URL 是 `https://github.com/example/repo.git`，那么命令将是：
     ```bash
     git clone https://github.com/example/repo.git
     ```

4. **进入项目目录**：
   - 克隆完成后，你可以通过 `cd` 命令进入项目文件夹：
     ```bash
     cd repo
     ```

## 将本地修改后的内容上传到 GitHub 仓库可以通过以下步骤完成：

1. **进入项目目录**：
   - 在终端中进入项目的文件夹（如果还没进入）：
     ```bash
     cd /path/to/your/project
     ```

2. **检查当前修改状态**：
   - 输入以下命令查看有哪些文件被修改或新增：
     ```bash
     git status
     ```

3. **添加修改后的文件**：
   - 如果想添加所有修改过的文件，可以使用以下命令：
     ```bash
     git add .
     ```
   - 如果只想添加特定文件，可以用文件路径代替 `.`，例如：
     ```bash
     git add filename
     ```

4. **提交更改**：
   - 提交文件，并添加提交信息（提交信息描述你的修改内容）：
     ```bash
     git commit -m "描述你的修改内容"
     ```

5. **将更改推送到 GitHub**：
   - 把提交的更改上传到 GitHub 仓库的远程分支上（通常是 `main` 或 `master` 分支）：
     ```bash
     git push origin main
     ```
   - 如果你的仓库分支是 `master`，请将 `main` 替换为 `master`。

6. **（可选）输入 GitHub 认证信息**：
   - 如果这是你第一次推送，可能需要输入 GitHub 用户名和密码。如果启用了两步验证，请使用 GitHub 的 **Personal Access Token** 代替密码。
