# promising.ts
👸🏻 promise to give me anything

usage

~~~ tsx
import { promisingGetter } from "./promising.tsx" ;

promisingGetter
(
    new Promise<string>
    ((resolve, reject) => 
    {
        setTimeout
        (() => 
        {
            resolve("hello world");
        }, 3000);
    }), 400
)(
    () => { console.log(`... wait, plz ...`) ; } ,
    (error: any) => { console.log(`[Error] occurred ! ${error}`) ; } ,
    (result: string | undefined) => { console.log(`[Result] gotten : ${result}`) ; }
) ;
~~~

### desc

这是个由于研究 Typescript 中的轮询工具而形成的项目。

该工具允许你给异步任务 `then` 链的某个环节增加等待时的动作效果。
