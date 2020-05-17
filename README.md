# Problem with ts-jest - typings not updated

Steps to reproduce:
 - run jest with watch `$ npm test -- --watch`
 - go into `src/add.test.ts` and edit the import from `add1` to `add2` in both import and where the function is used
 - see the error:
   ```
  FAIL  src/add.test.ts
  ● Test suite failed to run

    src/add.test.ts:1:10 - error TS2305: Module '"./add"' has no exported member 'add2'.

    1 import { add2 } from "./add";
   ```
 - go into `./add` and fix the function to be called `add2`.
 - see that the jest runner still say the same error
 - restart the runner and see it works now
