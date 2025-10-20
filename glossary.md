#  Glossary

**Router**
A router is just an object that groups together backend procedures (functions) in tRPC.

**Procedure**
A procedure is a backend function exposed to the frontend through tRPC (like an API endpoint).

**createTRPCRouter**
A factory function that creates a router object and registers all your procedures.

**publicProcedure / baseProcedure**
A starting template (builder) for defining a procedure that can be configured with `.input()` and `.query()`.

**Method chaining**
A pattern where functions return `this` so you can stack configuration calls like `.input().query()`.

**.input()**
Used to define and validate what data a procedure accepts using Zod schemas.

**.query()**
Creates a read-only tRPC procedure (like a GET request in REST) that returns data.

**Zod**
A validation library used in tRPC to define input schemas and ensure type safety.

**appRouter**
The main tRPC router that holds all of your backend procedures.

**typeof appRouter**
Creates a TypeScript type from the appRouter, used to give full type safety to the frontend.

**tRPC**
A system that lets the frontend call backend functions directly with full type safety, no REST routes required.

**Context (`ctx`)**
An object passed to every procedure that holds per-request info like auth/session/db access.

**createTRPCContext**
Function that builds and returns the `ctx` object for each request.

**useTRPC / trpc client**
A frontend hook/object generated from `appRouter` that lets React components call backend procedures.

**React Query**
A caching + data fetching library used by tRPC for queries and automatic state management.

**QueryClient**
The central React Query cache that stores data from queries so they don't refetch unnecessarily.

**Prefetch**
Fetching data before it’s needed so the UI feels faster when rendered.

**Hydration**
Reusing server-fetched data on the client to avoid refetching after SSR.

**Dehydration (`dehydrate`)**
Converting server-side React Query cache into JSON so it can be sent to the browser and rehydrated.

**HydrationBoundary**
A React Query component that restores dehydrated data back into a working cache on the client.

**useSuspenseQuery**
React Query hook that pauses rendering (using React Suspense) until data is ready, removing the need for manual `isLoading` checks.
