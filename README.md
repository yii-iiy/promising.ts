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

这是个练手项目。

它会允许你给你的异步任务的 `then` 链的某个环节增加等待效果，并且仍然能对成功和失败的情况做出不同操作。
