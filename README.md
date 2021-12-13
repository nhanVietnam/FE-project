Yêu cầu: 
- Node.js >= v16.13.1: https://nodejs.org/en/ 

Kiến thức cần có:
- Typescript
- SCSS
- Expressjs (căn bản)

Hướng dẫn setup project: 

# Setup cấu trúc folder và webpack để build ra demo

- Tạo folder project đặt tên túy ý 

- Vào project chạy lệnh cài webpack “npm install webpack” 

- Chạy lệnh init project “npm init –y” 

- Tạo file .gitignore ở folder project xong ghi vào đó “node_modules” để bỏ folder node_modules ra khi push lên git 

- Chạy lệnh “npx webpack init" để khởi tạo webpack, khi chạy xong sẽ cần chọn các option trong terminal như sau: 

    + Would you like to install '@webpack-cli/generators' package? (That will run 'npm install -D @webpack-cli/generators') (Y/n): y

    + Which of the following JS solutions do you want to use?: Typescript

    + Do you want to use webpack-dev-server?: n

    + Do you want to simplify the creation of HTML files for your bundle?: n

    + Do you want to add PWA support?: n

    + Which of the following CSS solutions do you want to use?: SASS

    + Will you be using CSS styles along with SASS in your project?: y

    + Will you be using PostCSS in your project?: y

    + Do you want to extract CSS for every file?: Yes

    + Do you like to install prettier to format generated configuration?: y

    + Overwrite package.json?: y

- Vào file package.json đổi biến “name” thành tên của project

- Tạo file, folder trong folder "src"

    + Tạo folder "ts": Tất cả file typescript viết vào đây

    + Tạo folder "scss": Tất cả file scss viết vào đây

    + Tạo file index.scss: import tất cả scss vào đây

    + File "index.ts" đã được tạo sẵn: dùng để import index.scss vừa tạo và tất cả file typescript, build xong chạy demo để a xem

- Tạo folder assets trong folder gốc của project: các hình ảnh cần dùng trong demo bỏ hết vào đây

# Setup server expressjs để chạy demo

- Cài expressjs bằng lệnh "npm install express"

- Tạo file "app.js" ở folder gốc của project

- Tạo file "index.html" trong folder "assets" vừa được tạo và tạo tag <script src="/assets/main.js"/> ở cuối body

- Vào file "app.js" mới tạo serve file "index.html" vừa tạo ở trên ở port 8001 kèm với tất cả hình ảnh trong folder "assets"

    + Nếu k biết tạo thì vào github của a mà copy code vô: https://github.com/tunanyugen/project-template

- Chạy lệnh "npm run build" để build project
    + Lệnh trên sẽ tạo folder "dist" trong folder gốc của project và compile tất cả code dc import trong file "index.ts" sẽ compile vào file "main.js" trong folder "dist"

- Chạy thử demo bằng lệnh "node app.js" xong vào url "localhost:8001"

- Khi vào được demo thì bấm F12 để xem trong console có log ra "Hello World!" hay k, nếu k có thì setup sai r :v

# NOTE
- Thắc mắc gì thì tự google, hỏi mấy câu trên google có thì a sẽ k trả lời đâu nghe!