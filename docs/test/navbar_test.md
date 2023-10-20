# Frontend Test Case for Login Component

## Objective

The objective of this test is to verify the rendering behavior and functionality of the `Login` component with provided props.

## Test Description

### Test Setup

1. **Component Under Test (CUT):** `Login` component.
2. **Testing Library:** Enzyme for React component testing.
3. **State Management:** Redux is used with a store configured using `configureStore`.
4. **Provided Props:** An object `login` containing email and password, and an object `location` containing state information.

### Test Steps

1. **Create Redux Store:**
   - A Redux store is created using the `configureStore` function to provide state management for the component.

2. **Define Mock Props:**
   - A `login` object is defined to simulate email and password.
   - A `location` object is defined to mimic location state.

```bash
const auth = {
   isLoggedIn:"test"
}

const user = {
   name:"test",
   role:"test"
}
```

3. **Render Component with Provider:**
   - The `Login` component is shallow rendered using Enzyme's `shallow` method.
   - It is wrapped in a `Provider` to supply the Redux store.

4. **Take Snapshot:**
   - Jest's `toMatchSnapshot()` function is used to create a snapshot of the rendered component.
   - The snapshot serves as a baseline for future comparisons.

### Expected Output

- The expected output is that the rendered component matches the previously saved snapshot. This indicates that the component renders correctly with the provided props.

## Running the Test

To execute this test, use the appropriate testing command in your project. For example, if Jest is the testing framework, you can run:

```bash
npm test
```

Result output received upon testing this frontend api

![image](https://github.com/drs1951/CSC510_Group31/assets/85347670/85a7fdd2-9505-4401-aed1-93f76c4b98d9)
