# Next Modern Snippets

![Version](https://img.shields.io/visual-studio-marketplace/v/xansiety.next-modern-snippets)
![Installs](https://img.shields.io/visual-studio-marketplace/i/xansiety.next-modern-snippets)
![License](https://img.shields.io/github/license/Xansiety/next-modern-snippets)

Modern snippets for React and Next.js 15+ development. Built for the latest patterns including async params, server components, and React 19 features.

## Snippets

| Prefix   | Name                            | Description                                          |
| -------- | ------------------------------- | ---------------------------------------------------- |
| `prc`    | Page Component                  | Simple page component                                |
| `prcfc`  | Functional Component (FC)       | Arrow function with `React.FC<Props>`                |
| `prca`   | Async Server Component          | Server component with async data fetching            |
| `prch`   | Custom Hook                     | Hook with `useState` and `useEffect`                 |
| `lmrc`   | Layout with Metadata            | Layout component with `Metadata` export              |
| `lrc`    | Layout without Metadata         | Layout component without metadata                    |
| `crc`    | Client Component                | Component with `"use client"` directive              |
| `mr`     | Static Metadata                 | Static `Metadata` export                             |
| `gmrf`   | Generate Metadata               | `generateMetadata` function for dynamic SEO          |
| `gsp`    | Generate Static Params          | `generateStaticParams` function                      |
| `ldc`    | Loading Component               | Loading UI component                                 |
| `err`    | Error Component                 | Error segment with reset functionality               |
| `ebc`    | Error Boundary                  | React 19 `ErrorBoundary` wrapper component           |
| `prcsp`  | Page with searchParams          | Async page with params and searchParams (Next.js 15+)|

## Usage

Type a snippet prefix (e.g. `prc`) in a `.tsx` or `.jsx` file and press <kbd>Tab</kbd> to expand.

### Tab Stops

Snippets use tab stops to let you quickly fill in key values:

- **`$1`** — Component name. Pre-filled with the PascalCase version of your filename (e.g. `product-list.tsx` becomes `ProductList`). Mirrored everywhere the name appears (declaration, JSX, export).
- **`$2`, `$3`** — Secondary fields like Props type contents, destructured params, metadata values.
- **`$0`** — Final cursor position after all tab stops are filled.

Press <kbd>Tab</kbd> to move to the next stop. Edit `$1` once and all mirrored instances update together.

## Next.js 15+ Notes

This extension follows Next.js 15+ conventions:

- **`params` and `searchParams` are Promises.** In Next.js 15+, dynamic route parameters are async. The `prcsp` and `gmrf` snippets use `Promise<{ slug: string }>` and `await params` to match this pattern.
- **Server components are the default.** The `prca` snippet creates an `async function` component for server-side data fetching without any directive.
- **Client components require `"use client"`.** The `crc` and `err` snippets include the directive at the top.

## Supported Languages

- TypeScript React (`.tsx`)
- JavaScript React (`.jsx`)

## Contributing

Contributions are welcome! To add or modify snippets:

1. Fork this repository
2. Edit `snippets/snippets.code-snippets`
3. Test your changes by pressing <kbd>F5</kbd> in VSCode to launch the Extension Development Host
4. Submit a pull request

## License

MIT
