**设计原则**
- 命名规范
- - 文件 // --
- - 脚本 // GameManager 与类名一致
- - 节点 // --
- -
- 通用模块设计
- - InputManager   ` // 管理设备输入， 将数据规范成 Axis: cc.v3(), trigger: boolean `
- - AnimationManager   ` // 导入resources/animation下的clip文件并保存在AnimationClips中，同时提供`
- - PrefabManager
- - AudioManager
- -
- 游戏模块设计
- - PlayerControl

```
    PlayerControl { //通过Input数据，驱动Animator改变Status, 播放对应AnimationClip
        _maxSpeed: number,
        _health: number,
        _attackValue: [],
        _heavyAttackIndex: [],

        Input { Axis, triggers},
        Animatior { Status, AnimationClips},
    }
```
- - AttackBox
- -
### **todo**
### 2021/3/6 17:06
1. **调整Main界面UI动画**
2. 增加预制体资源导入管理模块
3. 关卡设计
4. 故事设计

### **done**
### 2021/3/8 13:10
1. 增加血条
2. 调整角色节点布局
3. 优化AttackBox.ts
4. 调整UI动画
5. 修复带有刚体组件的子物体不跟随父物体移动的bug
