# Import Statements

## Avoid documenting and grouping import statements with comments
Most IDEs and code editors have auto-import support. This results in import statements getting added
and updated by tooling. When we attempt to manually manage these or document these it puts added work and time
in the next developer's workflow to curate that as new imports get added. Or, it results in it not being done
and these get out of sync.

### 🚫 Avoid
```typescript
// ===============================================================================
// Internal Features (Store)
import { AppState } from './state';

// ===============================================================================
// External Features (Data Services)
import { AccountModel } from '@my-project/services';

// ===============================================================================
// Libs
import { createSelector, MemoizedSelector } from '@ngrx/store';
import { getAccountState } from './selectors';
```

### ✅ Do
```typescript
import { AppState } from './state';
import { AccountModel } from '@my-project/services';
import { createSelector, MemoizedSelector } from '@ngrx/store';
import { getAccountState } from './selectors';
```
