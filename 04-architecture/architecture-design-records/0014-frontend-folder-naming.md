# Frontend folder naming

* Status: <Draft, To be discussed, Under Consideration, Accepted>
* Deciders: [names]
* Date: <date>

## Context and Problem Statement
As the project organically grew, adhoc decision were made around the naming of the folders, eventually leading to small inconsistencies between the domains. 

At the time of writing the structure is as follows:
- `app/customer/customer-edit-page/CustomerEditPage.tsx`
- `app/product/product-search-page/ProductSearchPage.tsx`

We want an improved and agreed upon way of naming our directories moving forward.

## Suggested Solution
The suggestion was made to make the folder naming more concise; removing the domain prefix and the page suffix in the folder naming, while keeping the file names and exports as is to preserve searchability.

The following change was suggested:
- `app/customer/customer-edit-page/CustomerEditPage.tsx` -> `app/customer/edit/CustomerEditPage.tsx`
- `app/product/product-search-page/ProductSearchPage.tsx` -> `app/product/search/ProductSearchPage.tsx`

To be added domains e.g. Order could be implemented using to the following naming convention:

```
product/
  ├── ...
customer/
  ├── ...
order/
  ├── view/
  │     ├── details/
  │     │      └── OrderDetails.tsx // only used by OrderViewPage
  │     └── OrderViewPage.tsx
  ├── create/
  │     └── OrderCreatePage.tsx
  ├── edit/
  │     └── OrderEditPage.tsx
  └── search/
        └── OrderSearchPage.tsx
```

## Decision Outcome
We've agreed on the suggested change of more concise naming for folders; by removing the domain and page prefix in the directories.
