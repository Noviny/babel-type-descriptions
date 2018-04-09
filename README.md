The goal is to have a link to ASTexplorer to demonstrate what each type is. Types have been broken into sections if they are not core parts of javascript (JSX, type annotations, typescript types), however are otherwise in alphabetical order.

WIP - un-added types have a leading `^^^^` while I am working on them.

## Important Base Parts

### Knowing these will help everywhere

- [identifier](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/e4328d6bf0d3edf2813588158c22e7d1b8089b34) A named property, such as a declared variable or object property.
- [blockStatement](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/e68d5ef35ab471418c2bbca14a86d7c8ccf21db0) Anything to be run as part of resolving an expression. (Effectively anything that would go between {} brackets, whether that is in a for statement, or function expression. It will be found as the `body` property of the expression.
- **file** identifies that all code within the AST down from this comes from a single javascript file within the filesystem.
- **program** The body type of a file, under which the rest of the file's AST sits. (files may also have comments and tokens)
- [expressionStatement](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/3e793d7e3a9f2b338cfc8ff200c5c75d869a3bff) `func()`
- [variableDeclaration](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/5e216443d6bbb3d1812f741bf9999277c0f48869) `var a = 'a';` 
- [variableDeclarator](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/5e216443d6bbb3d1812f741bf9999277c0f48869) `var a = 'a';`

### Literal types

Literal types are javascript primitives. They are normally simple values.

- [booleanLiteral](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/081357a73245e9614de4a8e648d989affabfb79c) `true` or `false`
- [directiveLiteral](https://astexplorer.net/#/gist/042bfc14d1c5ddc0416a96c70fef123e/7760506d77d2bda099524656e48e9a5c87284806) `"use strict"`
- [nullLiteral](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/1a0a445f3f4ca041a9aabb1298a6c89865f000af) `null`
- [numericLiteral](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/2e58a0d7d4300cc81081003f57cd6a570dd948a0) Any number
- [regExpLiteral](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/d78c9e6eab9cf47f799b5a275d4ddcd4a6d19d31) `/asdf/`
- [stringLiteral](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/2f69eaf2deede9809879e0672bf8f3ac86ebfca1) `'this kind of thing'` or `"this kind of thing"`
- [templateLiteral](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/bc36b514942019044d47ab215f50a92716b3eed5) `` `something like this` ``

### Expressions

Expressions can be seen as taking an action, whether adding a new 

- [arrayExpression](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/06d1363f150aeeaa7c5c880e9feccb155ece5229) `['a']`
- [arrowFunctionExpression](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/d56fde3ce743d838c8316e8668c61381d14b0291) `() => {}`
- [assignmentExpression](https://astexplorer.net/#/gist/720e7837ea29f3b572d4028560ec01a4/9854c53a8512df3bd3185ab181f98f418207df10) `a = 1 + 2` Assignment outside of an initial instantiation (reassigning a variable, or object property)
- [awaitExpression](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/6aadd54246dd4c303852ab6dc8305d310148cd66) `await func()`
- [binaryExpression](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/f5f954f458957300ff6f19eaeea51192206ec5da) An operation with two sides, such as base mathematical operations or concatenation
- [bindExpression](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/c7bac3fc0079cd3208321a07ec954e9ce1f91277) `let a = ::b.c`
- [callExpression](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/081357a73245e9614de4a8e648d989affabfb79c) `func()`
- [classExpression](https://astexplorer.net/#/gist/042bfc14d1c5ddc0416a96c70fef123e/f5773b44ab1ab4d952427d21980fcd9783c9b7af) `var foo = class {}`
- [conditionalExpression](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/ec387a1e264b3b03f0943c18d7b560722c266970) `a ? b : c`
- [doExpression](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/dc246c69e1f3677f986073907ed5dbddcf336e7f) `let a = do {}`
- [functionExpression](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/6bbae4e80de1b6154cde2597d65375664b47e6c2) `var x = function() {}`
- [logicalExpression](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/4dc060697730d3961fd892d05c72ab52ff60eca8) `a || b` or `a && b`
- [memberExpression](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/3e0dfeb927f168f3c940f147051510d028d38bc7) `a.b()`
- [newExpression](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/4259f9e2e0b9f2b1171a91624281a5e7be6aeab8) `new a`
- [objectExpression](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/72dd444305e89cc4be44ed2ef9869c5e98931dbd) `const a = {}`
- ^^^^[parenthesizedExpression]()
- [sequenceExpression](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/1c4373ddd4c3c766a375202b42df1eaf425c351d) `(1, 2, 3)` 
- [taggedTemplateExpression](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/997cdf153d841693a2a011879c617ab1902effea) `` func`a` ``
- [thisExpression](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/ec387a1e264b3b03f0943c18d7b560722c266970) `this`
- [unaryExpression](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/5613db81e87c74eb1849da518d9175d296be5cca) Operators with a single argument; `typeof` or `delete`
- [updateExpression](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/0f8b5a9e6427a3fa20b47902809a96dba3eae36c) `++a`
- [yieldExpression](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/ed0432c15935585f8a523826da582d386e7313c2) `function* a () { yield b }`

(possible other bits)
### Declarations (declarators?)
### Statements
### Patterns

## Javascript Properties


- [arrayPattern](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/585aab562c29b682a3bf3ca4044c498df1e7f64e) `function a ([ b, c ]) {}`
- [assignmentPattern](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/f81c9cd043989ee949ad527b16a99e98e98c43ad) `function a (b = 1) {}`
- [breakStatement](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/e10d259e44fc2937448213ab27f6d8e5dcaee7a6) `while (true) { break }`
- [catchClause](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/005c81e305f507de314e21683b4a62a10edccb8a) `try {} catch (e) {}`
- [classBody](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/248d0cb28deff788138cd85529a93d9405925b73) The body of a classDeclaration
- [classDeclaration](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/819661c346f629fae35bfe69d42a07e45b80ac3f) `class a {}`
- [classImplements](https://astexplorer.net/#/gist/5f72ca8e396f4c076b8f7125f7c11e0f/938c86d93d1bcf71d895ae4c7327a5d6e975e160) `class a implements b {}`
- [classMethod](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/cbf3c99bca29d8a3c37be32f16d2a391c33a77c5) `class b { constructor() {} }` the constructor is an example of a class method
- [classProperty](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/248d0cb28deff788138cd85529a93d9405925b73) Assigned property within a class
- [continueStatement](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/82b2b1f66ebdf2bff9ce15cf22d01006f1718503) `while (true) { continue }`
- [debuggerStatement](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/d43686adb8b67fd643ed3027864b3b34500eddee) `debugger`
- [decorator](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/1ab5288c23865b09473cc09a524c2bb27eb1457e)
- [directive](https://astexplorer.net/#/gist/042bfc14d1c5ddc0416a96c70fef123e/7760506d77d2bda099524656e48e9a5c87284806) `"use strict"`
- [doWhileStatement](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/265ef122e112bb11dd104800bb99df6de95a4270) `do {} while (true)`
- ^^^^[emptyStatement]()
- [exportAllDeclaration](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/b3acb21bef4dbabe3f58c288a8436255ebc8e3c4) `export * from './place';`
- [exportDefaultDeclaration](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/acb9eaec362daea50b151e445f5eca269e1960ac) `export default a`
- ^^^^[exportDefaultSpecifier]()
- [exportNamedDeclaration](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/8b66f55dace811a7ef577a7a4223b299559a6994) `export { a }`
- ^^^^[exportNamespaceSpecifier]() 
- [exportSpecifier](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/375f3b4c4944b4b8b238baa971cc83040c1f59f4) `export { a as b }`
- [forInStatement](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/d4f2e0a80b1db3f580dd58f6d13d18d3745946f4) `for (let a in b) { /* do something over an object's properties */ }`
- [forOfStatement](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/3b63012d3f2b58d79e569b62ccf30110ed8e34d7) `for (let a of b) { /* do something over an array's items */ }`
- [forStatement](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/7d3c002c0862f7b254b8b15f782e95575a662014) `for (var i = 0; i < val; i++) {}`
- [functionDeclaration](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/19802fd407286e17ee5575b1ef7d089e894fc726) `function a () {}`
- [ifStatement](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/0dec274f6a001414cf9f53dfcba41b082f89e786) `if (true) {}`
- ^^^^[import]()
- [importDeclaration](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/e3d0cc8a90697e789ab03d4823b0bff6e5708816) `import a from 'a'`
- [importDefaultSpecifier](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/e3d0cc8a90697e789ab03d4823b0bff6e5708816) `import a from 'a'`
- [importNamespaceSpecifier](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/477e6db39c64561ba5b4d8abc6d725fad2a88bb4) `import * as a from 'a'`
- [importSpecifier](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/c75f32d3979b7ee6d2a11ac1c6021161ef1cf8ce) `import { a } from 'a'`
- ^^^^[inferredPredicate]()
- ^^^^[interfaceDeclaration]()
- ^^^^[interfaceExtends]()
- ^^^^[labeledStatement]()
- ^^^^[metaProperty]()
- ^^^^[noop]()
- [objectMethod](https://astexplorer.net/#/gist/7c86b693a649f6cb4f4eb5943d8b3d5f/b535b4ec48db7344b95f410b9358b55740d9bd7f) `let a = { a () {} }`
- [objectPattern](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/97be88a9a5621b45d0a6e90f13d3968e69e0475b) `function a ({ b }) {}`
- [objectProperty](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/8d1fd8d3b0b7c5a89855982c976c6f41bd661046) Any value added to an object.
- [restElement](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/7cea9274151d097ff25ebcefe0a2deebe6c30e77) `function a (...a) {}`
- [returnStatement](https://astexplorer.net/#/gist/9952dc650522941e0229e6ea90c11a99/2f69eaf2deede9809879e0672bf8f3ac86ebfca1) `() => { return }`
- [spreadElement](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/d0b3d7cce992d8debc10c31fb7702c350adeccd5) `let a = [...b]`
- [super](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/662053987a2bbbf95076f37d25fac4a9c42e0978) `class a extends b { constructor () { super() } }`
- [switchCase](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/c09e163ff94a1593e4c77bce1cf4f6db6f74e5b4) `case a: // the case results`
- [switchStatement](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/c09e163ff94a1593e4c77bce1cf4f6db6f74e5b4) the whole switch statement beginning with `switch (a) {`
- [templateElement](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/319932ed9b15451e0a54ef8a29d46e1395d60aaa) `ab`
- [throwStatement](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/e07480310dda6781c56917f47b407cf3aeff585a) throw `a`
- [tryStatement](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/57b65433b5e699c6c88fbb0ba76c17127031429c) `try {} catch (e) {}` or `try {} finally {}`
- [whileStatement](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/2f8d7a528c7871e97d3956e9ad30a686f66b13b1) `while (true) {}`
- [withStatement](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/ed91ecaef71d46bd864a8a546792c57fd024de83) mdn recommends don't use with statements.

## JSX Properties

These are parts of JSX syntax. For more information on JSX, please see the [react documentation]().

- [jSXAttribute](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/9a9e3d2c51b76aa38ed0bcaad3490bdf26536d8b) `<B c="c" />`
- [jSXClosingElement](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/f4a144927b8478f96089c986d7c1197bfb0ef33a) `<div>a</div>`
- [jSXClosingFragment](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/2fc80618035d15f90c4b4eb79d16f3633d6cbdc1) `<></>`
- [jSXElement](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/f4a144927b8478f96089c986d7c1197bfb0ef33a) `<div>a</div>`
- [jSXEmptyExpression](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/ff4ee8301b86396272e53b14000fa9a575b00d47) `<B>{}</B>`
- [jSXExpressionContainer](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/f75dfaf0db68fda3804a0ded23521c84f8dd661c) `<B c={c} />`
- [jSXFragment](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/2fc80618035d15f90c4b4eb79d16f3633d6cbdc1) `<></>`
- [jSXIdentifier](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/6a56ff7589198879097ac2115221c5be4603e854) `<B />`
- ^^^^[jSXMemberExpression]()
- ^^^^[jSXNamespacedName]()
- [jSXOpeningElement](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/f4a144927b8478f96089c986d7c1197bfb0ef33a) `<div>a</div>`
- [jSXOpeningFragment](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/2fc80618035d15f90c4b4eb79d16f3633d6cbdc1) `<></>`
- [jSXSpreadAttribute](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/f5c3b0a19549fdf8f796589559e65b458a39f109) <B {...c} />
- [jSXSpreadChild](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/1716bfb4a74ce740c5ac6176ea787da896fcc3a1) `<B>{...c}</B>`
- [jSXText](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/f4a144927b8478f96089c986d7c1197bfb0ef33a) `<div>a</div>`

## Other Types Bits

## Type types

These properties are used for typing systems, mostly flow.

- [typeCastExpression](https://astexplorer.net/#/gist/16cb18fe2bd518ead4b2079f269f0619/493421d90edbce1ed4f8e6511208066f2beadfc4) `func(a: string)`
- [functionTypeParam](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/92e597c2c5ba0afe496c0b2d97b21207d0b08b85) `type a = (b: string) => mixed`
- [opaqueType](https://astexplorer.net/#/gist/16cb18fe2bd518ead4b2079f269f0619/d9c87c6dee679015d8e4e3c45131fdb700697063) `opaque type a = string;`
- ^^^^[qualifiedTypeIdentifier]()
- [typeAlias](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/7f561ed66b55be5aa1e926ccb297b6211c0916b6) `type a = string`
- [typeAnnotation](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/d2e152d27ccd3b91146b34f6171754044f1cad26) `let a: string = 'a'`
- ^^^^[typeParameter]()
- ^^^^[typeParameterDeclaration]()
- [typeParameterInstantiation](https://astexplorer.net/#/gist/2a4894efe8c197f5b0102d749688bb96/8736f11b70a2e20724426e7a50315558f312c484) `type a = A<*>`
- ^^^^[objectTypeCallProperty]()
- ^^^^[objectTypeIndexer]()
- [objectTypeProperty](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/eaff424549f75b4d55bbe2102d0c81a102cf315c) `type a = { b: string }`
- [objectTypeSpreadProperty](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/ebf397132a05d64b06e706f44a74d6a99b65feee) `type a = { ...string }`

### Declarations

- [declareClass](https://astexplorer.net/#/gist/9bdbb085011c700a94b5786e5f239e0a/04c4f5ea3caeb76082ef750b51a5468165da68d0) `declare class a {}`
- ^^^^[declareExportAllDeclaration]()
- [declareExportDeclaration](https://astexplorer.net/#/gist/9bdbb085011c700a94b5786e5f239e0a/b4d9da6852a4ae45280470d1414fa3abf3d9a0f5) `declare export default boolean`
- [declareFunction](https://astexplorer.net/#/gist/9bdbb085011c700a94b5786e5f239e0a/e7e1dcabe5e5c0405ae79c8bde49e961df6d646b) `declare function a(b: number): string;`
- ^^^^[declareInterface]()
- [declareModule](https://astexplorer.net/#/gist/9bdbb085011c700a94b5786e5f239e0a/d05cd84cee1a98dfe4d90cf0e82a8c801457438b) `declare module 'a' {}`
- ^^^^[declareModuleExports](https://astexplorer.net/#/gist/b1ced96dd1681521a0214ed90eaf50d3/3e5a819ef1190933ab6eb16e2e00525ac042ceeb) `declare module.exports: 'a';`
- ^^^^[declareOpaqueType]()
- [declareTypeAlias](https://astexplorer.net/#/gist/9bdbb085011c700a94b5786e5f239e0a/d3312cd0dbb8f69fa36e2032a8f563d2f478e55d) `declare type a = boolean`
- [declareVariable](https://astexplorer.net/#/gist/9bdbb085011c700a94b5786e5f239e0a/71caaee670542fab09a38fc5d373cddd39079b8b) `declare var a: boolean`
- ^^^^[declaredPredicate]()

## Type Annotations (most likely flow)

These type annotations are the kind used in flow. I recommend reading the [flow documentation]() to understand these types. Each will be found within a **typeAnnotation** property for an identifier.

- [anyTypeAnnotation](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/771b8f78962d6d236e39da0b7a40b968c93f172d) `type a = any;`
- [arrayTypeAnnotation](https://astexplorer.net/#/gist/16cb18fe2bd518ead4b2079f269f0619/5b48431035d6a8651536bd3fac9f511cd4755645) `type a = number[]`
- [booleanLiteralTypeAnnotation](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/4b9407e3df61373d273edce8c356b40658adf209) `type a = true`
- [booleanTypeAnnotation](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/aa41fddb013ff0efbfafbdb1b5ff922ed4ea1988) `type a= boolean`
- ^^^^[emptyTypeAnnotation]()
- [existsTypeAnnotation](https://astexplorer.net/#/gist/2a4894efe8c197f5b0102d749688bb96/0fba998b1474ea8332f1fca97bf794db1263617b) `type a = *`
- [functionTypeAnnotation](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/596b2ff78af86b0c1091ac9382eaed955fe78a47) `type a = () => {}`
- [genericTypeAnnotation](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/da6bb3a05e4ba8f8fd2c3ebc91682c2e29d889ba) `type a = b`
- [intersectionTypeAnnotation](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/d8fcf1ef10df8a2c9363c7df1bfb8014630885f3) `type a = string & 'a'`
- [mixedTypeAnnotation](https://astexplorer.net/#/gist/16cb18fe2bd518ead4b2079f269f0619/b1c62b40659f26f73032b0fa92618c4181bb6d68) `type a = mixed`
- [nullLiteralTypeAnnotation](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/d40f037cca44b66ecb4332f1d9eb47ac22fa3276) `type a = null`
- [nullableTypeAnnotation](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/0f2773c675a02f1a41890a2f151e9e0fea8762d6) `type a = ?string`
- [numberLiteralTypeAnnotation](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/a662ac950549f8c12bd492270684d6a72d678356) `type a = 5`
- [numberTypeAnnotation](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/ae26a6f6b6f659ed9431856f61133ba7f0e903a0) `type a = number`
- [objectTypeAnnotation](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/15bc9efdc073097f558204541297e2dca929eda4) `type a = {}`
- [stringLiteralTypeAnnotation](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/4ca2c206fe69ab1c08bb4f57c43878fae7f75749) `type a = 'a'`
- [stringTypeAnnotation](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/c8c2ab05e254bf2cea6976d2948b6e95dee612f7) `type a = string`
- [thisTypeAnnotation](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/bf3084d620a46557a07eea7bee4480da707f4f1f) `type a = this`
- [tupleTypeAnnotation](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/dae58736c274f3780837699b9e194b1bb93bd715) `type a = [b, c]`
- [typeofTypeAnnotation](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/6f37a762b615f747b64b1b6750b80ff7cd7f6820) `type a = typeof b`
- [unionTypeAnnotation](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/2b3c6f75e53ab57cc31118752aba2b6095e33806) `type a = string | number`
- [voidTypeAnnotation](https://astexplorer.net/#/gist/2cfeccb1d1c16589b2de69097b0b700f/bb46be228a2e09fdb5e828d349c890a9a49d0242) `type a = void`

## Typescript Types

- ^^^^[tSAnyKeyword]()
- ^^^^[tSArrayType]()
- ^^^^[tSAsExpression]()
- ^^^^[tSBooleanKeyword]()
- ^^^^[tSCallSignatureDeclaration]()
- ^^^^[tSConstructSignatureDeclaration]()
- ^^^^[tSConstructorType]()
- ^^^^[tSDeclareFunction]()
- ^^^^[tSDeclareMethod]()
- ^^^^[tSEnumDeclaration]()
- ^^^^[tSEnumMember]()
- ^^^^[tSExportAssignment]()
- ^^^^[tSExpressionWithTypeArguments]()
- ^^^^[tSExternalModuleReference]()
- ^^^^[tSFunctionType]()
- ^^^^[tSImportEqualsDeclaration]()
- ^^^^[tSIndexSignature]()
- ^^^^[tSIndexedAccessType]()
- ^^^^[tSInterfaceBody]()
- ^^^^[tSInterfaceDeclaration]()
- ^^^^[tSIntersectionType]()
- ^^^^[tSLiteralType]()
- ^^^^[tSMappedType]()
- ^^^^[tSMethodSignature]()
- ^^^^[tSModuleBlock]()
- ^^^^[tSModuleDeclaration]()
- ^^^^[tSNamespaceExportDeclaration]()
- ^^^^[tSNeverKeyword]()
- ^^^^[tSNonNullExpression]()
- ^^^^[tSNullKeyword]()
- ^^^^[tSNumberKeyword]()
- ^^^^[tSObjectKeyword]()
- ^^^^[tSParameterProperty]()
- ^^^^[tSParenthesizedType]()
- ^^^^[tSPropertySignature]()
- ^^^^[tSQualifiedName]()
- ^^^^[tSStringKeyword]()
- ^^^^[tSSymbolKeyword]()
- ^^^^[tSThisType]()
- ^^^^[tSTupleType]()
- ^^^^[tSTypeAliasDeclaration]()
- ^^^^[tSTypeAnnotation]()
- ^^^^[tSTypeAssertion]()
- ^^^^[tSTypeLiteral]()
- ^^^^[tSTypeOperator]()
- ^^^^[tSTypeParameter]()
- ^^^^[tSTypeParameterDeclaration]()
- ^^^^[tSTypeParameterInstantiation]()
- ^^^^[tSTypePredicate]()
- ^^^^[tSTypeQuery]()
- ^^^^[tSTypeReference]()
- ^^^^[tSUndefinedKeyword]()
- ^^^^[tSUnionType]()
- ^^^^[tSVoidKeyword]()
