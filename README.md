前端面试用题:

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>JS 测试部分</title>
    <style>
        .itemDiv span {
            display: inline-block;
            margin: 0 10px;
        }

        .cate {
            border-bottom: 1px solid #333;
            padding-bottom: 10px;
        }
        table{
            text-align: center;
            width: 100%;
        }
        td,th{
            border: 1px solid #999;
        }
        .bgGreen{
            background: green;
            color: #fff;
        }
        .bgRed{
            background: red;
            color: #fff;
        }
    </style>
</head>

<body>
    <div id="app">
        <div class="cate">
            <p>1. 数组排序：不使用sort方法，实现一个排序</p>
            <div class="itemDiv">
                <span v-for="item in arr">{{item}}</span>
                <button @click="sortArr">排序</button>
            </div>
        </div>
        <div class="cate">
            <p>2. 正则表达式：测试输入字符串是否为xxx-xxx-xxxx格式，其中x为数字</p>
            <input type="text" v-model="str"> <button @click="testReg">测试</button>
        </div>
        <div class="cate">
            <p>3. 求和：请将下列字符串中的数字进行求和</p>
            <div>"{{sumStr}}" <button @click="getSum">求和</button></div>
        </div>
        <div class="cate">
            <p>4. 数据处理：点击删除后，将不会该项运动的人移除。（具体请看数组中的数据情况）</p>
            <select v-model="keyOfTeam">
                <option value="">空</option>
                <option v-for="item in keys" :value="item">{{item}}</option>
            </select>
            <button @click="deleteKey">删除</button>
            <table>
                <tr>
                    <th v-for="item in tableHead" class="bgGreen">{{item}}</th>
                </tr>
                <tr v-for="man in team">
                    <td v-for="item in man" :class="{bgRed:!item}">{{item}}</td>
                </tr>
            </table>
        </div>
    </div>
</body>
<script src="./vue.js"></script>
<script>
    // 请不要编写vue实例中的data部分，只在methods下作答

    let vue = new Vue({
        el: "#app",
        data: {
            //第一题数据
            arr: [1, 3, 5, 7, 9, 2, 4, 6, 8],
            //第二题数据
            str: "787-123-1231",
            //第三题数据
            sumStr: "a,1,b,2,c,3,d,4,e",

            //第四题数据
            keys: ['badminton', 'football', 'tabletennis', 'basketball'],
            keyOfTeam: "football",
            tableHead: ['姓名', '棒球(badminton)', '足球(football)', '乒乓球球(tabletennis)', '篮球(basketball)'],
            team: [{
                name: "小明",
                badminton: false,
                football: false,
                tabletennis: true,
                basketball: true
            }, {
                name: "小华",
                badminton: true,
                football: false,
                tabletennis: true,
                basketball: true
            }, {
                name: "小李",
                badminton: true,
                football: true,
                tabletennis: false,
                basketball: true
            }, {
                name: "小赵",
                badminton: true,
                football: true,
                tabletennis: true,
                basketball: false
            }, {
                name: "小王",
                badminton: false,
                football: true,
                tabletennis: true,
                basketball: false
            }, {
                name: "小林",
                badminton: true,
                football: false,
                tabletennis: true,
                basketball: false
            }]
        },
        methods: {
            sortArr() {
                //  第一题
                // 请不要使用sort方法，自己实现排序，从大到小       

            },
            testReg() {
                //  第二题


            },
            getSum() {
                //  第三题

            },
            deleteKey() {
                //  第四题

            }
        }
    })
</script>

</html>