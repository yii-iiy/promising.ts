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
