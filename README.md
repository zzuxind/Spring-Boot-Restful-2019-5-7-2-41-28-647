## Spring Boot Restful

### 练习描述
- 在`UserController`中按照Restful API设计 来补全接口
```

@RestController
@RequestMapping("")
//ToDo:在上一行代码("")中填写合适的RestfulApi
public class UserController {

    @Autowired
    private UserService userService;

    @GetMapping("")
    //ToDo:在上一行代码("")中填写合适的RestfulApi
    public ResponseEntity getAllUser() {
        return new ResponseEntity<>(userService.getAllUser(), HttpStatus.OK);
    }

    @PostMapping("")
    //ToDo:在上一行代码("")中填写合适的RestfulApi
    public ResponseEntity addUser(@RequestBody User user) {
        userService.addUser(user);
        return new ResponseEntity(HttpStatus.CREATED);
    }

    @PutMapping("")
    //ToDo:在上一行代码("")中填写合适的RestfulApi
    public ResponseEntity updateUserById(@PathVariable int userId, @RequestBody User user) throws BusinessException {
        userService.updateUserById(userId, user);
        return new ResponseEntity(HttpStatus.NO_CONTENT);
    }

    @DeleteMapping("")
    //ToDo:在上一行代码("")中填写合适的RestfulApi
    public ResponseEntity deleteUserById(@PathVariable int userId) throws BusinessException {
        userService.deleteUserById(userId);
        return new ResponseEntity(HttpStatus.NO_CONTENT);
    }
}
```

### 环境描述
- java8
- Intellij-IDEA

### 如何开始
- 克隆模版库
- 启动项目，若出现 Tomcat started on port(s): 8080 (http) 字样，并打开`localhost:8080`页面后输出如下格式，说明项目启动成功。
```
[
    {
       id: 1,
       name: "小明"
    },
    {
       id: 2,
       name: "小红"
    },
    {
       id: 3,
        name: "小花"
    }
]
```


### 输出规范
-  在`UserController`中按照Restful API设计补全接口。
-  根据项目完 `增删改查` 功能
- 并且在项目根目录中添加 `增删改查`功能截图
