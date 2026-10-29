**Real problem:** agents that sat waiting on their own process, or repeated the same attempt over and over, burning quota.
**Before:** the turn limit was raised and the same attempt retried.
**After:** two checks without progress or a repeated error stop the work, and every brief closes within a maximum of three rounds with a verdict.
