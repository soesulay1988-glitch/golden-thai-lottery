# Preview Debug Notes

The public web home route renders Golden Thai content. Navigating to the lazy-loaded `/2d` route initially shows the in-app `ခဏစောင့်ပါ...` page loader and does not complete during the captured browser interaction. This is separate from the incorrect Expo preview shell shown on the phone screenshot and requires investigation of production lazy-load asset delivery or client-side runtime errors.

After the inline chat removal, the development `/2d` page renders the result, schedule, alert, prediction, and history sections without the duplicated in-page discussion/chat block. The header chat control remains available for the separate chat overlay.

The header Chat control opens the dedicated full-screen overlay and the browser console reports only development tooling/service-worker messages, with no application runtime error.

The refactored local `/2d` screen renders a visible `Chat` header button, a black-and-gold verified-result board, two 2D-only rows for 12:01 PM and 4:30 PM, and pending `--` placeholders. SET/VAL market values and the duplicated inline discussion section are absent. The install prompt can overlay the page in browser testing and is not part of the 2D result board.

After the black-and-gold header refactor, the browser click attempt on the visible header Chat control did not open the dedicated overlay in the captured state. This interaction must be investigated before the board checkpoint is prepared.

On the published home page, the navigation shell loads but the Thai Lottery result card remains in its loading/placeholder state. The browser console has no client-side runtime error, so the next investigation point is the public API/server response and deployment data access rather than the 2D UI markup.

After registering the scheduled routes and running the official-sync endpoint once, the local home page displays the restored published Thai Lottery draw for 1 September 2026, including first prize `417212` and last two digits `04`. The initial loader resolves into the expected result card.

The revised Myanmar 2D page renders the black-and-gold verified-result card, result schedule, session Hot placeholders, and the latest verified 3D value. SET/VALUE, Modern/Internet, and other market-number rows are absent. Current 2D results are pending for the day, so the page correctly renders `--` rather than fabricated values.

The black-and-gold page's header Chat button was tested after the design update. It opens the dedicated full-screen chat overlay successfully; the inline discussion section is not rendered in the normal 2D page flow.
