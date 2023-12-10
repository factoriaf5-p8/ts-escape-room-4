# Typescript Labs

## Lab 4: Optional Parameters

file: `/src/04-optional-params.problem.ts`

Our getName function has been refactored.

Now instead of taking in a single params object, it takes in first and last as individual parameters:

```ts
export const getName = (first: string, last: string) => {
  if (last) {
    return `${first} ${last}`;
  }
  return first;
};
```
This time TypeScript is telling us that in the first name test that it expected two arguments but only got one:


```ts
it("Should work with just the first name", () => {
  const name = getName("Matt");

  expect(name).toEqual("Matt");
});
```
If we update the first name test to call getName with "Pocock" as a second argument, the error will go away. However, the test would fail at runtime.

Challenge
Your challenge is to work out how to mark the last parameter as optional.