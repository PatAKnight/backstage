## API Report File for "@backstage/plugin-notifications-common"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
import { Config } from '@backstage/config';

// @public (undocumented)
export const getProcessorFiltersFromConfig: (
  config: Config,
) => NotificationProcessorFilters;

// @public (undocumented)
export type NewNotificationSignal = {
  action: 'new_notification';
  notification_id: string;
};

// @public (undocumented)
type Notification_2 = {
  id: string;
  user: string | null;
  created: Date;
  saved?: Date;
  read?: Date;
  updated?: Date;
  origin: string;
  payload: NotificationPayload;
};
export { Notification_2 as Notification };

// @public (undocumented)
export type NotificationPayload = {
  title: string;
  description?: string;
  link?: string;
  severity?: NotificationSeverity;
  topic?: string;
  scope?: string;
  icon?: string;
};

// @public (undocumented)
export type NotificationProcessorFilters = {
  minSeverity?: NotificationSeverity;
  maxSeverity?: NotificationSeverity;
  excludedTopics?: string[];
};

// @public (undocumented)
export type NotificationReadSignal = {
  action: 'notification_read' | 'notification_unread';
  notification_ids: string[];
};

// @public
export const notificationSeverities: NotificationSeverity[];

// @public (undocumented)
export type NotificationSeverity = 'critical' | 'high' | 'normal' | 'low';

// @public (undocumented)
export type NotificationSignal = NewNotificationSignal | NotificationReadSignal;

// @public (undocumented)
export type NotificationStatus = {
  unread: number;
  read: number;
};

// Warnings were encountered during analysis:
//
// src/filters.d.ts:4:22 - (ae-undocumented) Missing documentation for "getProcessorFiltersFromConfig".
// src/types.d.ts:2:1 - (ae-undocumented) Missing documentation for "NotificationSeverity".
// src/types.d.ts:4:1 - (ae-undocumented) Missing documentation for "NotificationPayload".
// src/types.d.ts:36:1 - (ae-undocumented) Missing documentation for "Notification".
// src/types.d.ts:73:1 - (ae-undocumented) Missing documentation for "NotificationStatus".
// src/types.d.ts:84:1 - (ae-undocumented) Missing documentation for "NewNotificationSignal".
// src/types.d.ts:89:1 - (ae-undocumented) Missing documentation for "NotificationReadSignal".
// src/types.d.ts:94:1 - (ae-undocumented) Missing documentation for "NotificationSignal".
// src/types.d.ts:98:1 - (ae-undocumented) Missing documentation for "NotificationProcessorFilters".
```