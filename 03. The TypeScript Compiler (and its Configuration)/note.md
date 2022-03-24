tsc app.ts --watch / -w - Watch Mode
tsc --init - Tạo TypeScript Project và tsconfig.json
tsc - Compile tất cả .ts File trong Project Folder thành .js File
4
{
"compilerOptions": {
"noEmitOnError": true, // Không compile .ts File thành .js File nếu có Error
},
"exclude": [
"node_modules" // mặc định
],
"include": [
"app.ts"
],
"files": [
"app.ts"
]
}
