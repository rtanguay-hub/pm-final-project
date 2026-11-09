# Mindmap: Daily Water Intake Tracker (Mobile App)

> Working title: **Sip**. A mobile app that helps people build and keep a healthy daily hydration habit.
> This mindmap covers three areas: **user needs**, **features**, and **potential problems**. Read the needs first, because every feature should trace back to one.

```mermaid
mindmap
  root((Sip Water Tracker))
    User Needs
      Know how much to drink
        Personal goal based on weight, age, activity
        Adjusts for weather and exercise
        Trustworthy guidance, not guesswork
      Remember to drink
        Busy days and deep focus
        Hard to notice thirst
        Gentle, not nagging
      Log with almost no effort
        Under 3 seconds per log
        No typing
        Works one-handed or hands-free
      See progress and stay motivated
        Clear view of today vs goal
        Streaks and trends over time
        A sense of accomplishment
      Health-driven needs
        Kidney stones or UTI prevention
        Pregnancy and breastfeeding
        Athletes and heavy sweaters
        Older adults with low thirst signal
        Fluid limits for heart or kidney patients
      Fit into existing life
        Sync with Apple Health and Google Fit
        Count coffee, tea, food water
        Privacy of health data
    Features
      Onboarding
        Profile: weight, activity, climate
        Recommended goal with explanation
        Pick bottle and cup sizes
      Logging
        One-tap quick add with presets
        Home-screen and lock-screen widgets
        Smartwatch complication
        Voice: Siri and Google Assistant
        Beverage types with hydration factor
        Undo and edit entries
      Smart Reminders
        Schedule within waking hours
        Adaptive: skip if already on track
        Pause in meetings via calendar
        Snooze and quiet hours
      Progress and Insights
        Daily ring or fill-the-bottle visual
        Weekly and monthly trends
        Best times and patterns
        Correlation with sleep, steps, mood
      Motivation
        Streaks with streak freeze
        Badges and milestones
        Optional friend or team challenges
        Positive, non-shaming copy
      Integrations
        Apple Health and Health Connect
        Wearables for workouts and heat
        Weather API for hot days
        Smart bottles via Bluetooth
      Settings and Data
        Units: ml and oz
        Export data as CSV
        Account and cloud backup
        Accessibility: large text, VoiceOver
      Monetization
        Free core tracking
        Premium: insights, themes, smart bottle sync
        No ads during logging
    Potential Problems
      Engagement
        Novelty wears off after 1 to 2 weeks
        Reminder fatigue leads to notifications off
        Forgetting to log, so data goes stale
        Broken streak causes churn
      Data Accuracy
        Users guess volumes
        Sips from shared bottles hard to count
        Double counting with Health sync
        Food and other drinks ignored
      Health and Safety
        Overhydration risk, hyponatremia
        Users on fluid restriction get wrong goals
        Implying medical advice
        Disclaimers and clinician mode needed
      Privacy and Compliance
        Health data is sensitive
        GDPR and CCPA consent
        App Store health data rules
        Third-party analytics leakage
      Business
        Crowded market, many free apps
        Low willingness to pay
        Platform built-ins like Apple Health
        Smart bottle hardware dependency
      Technical
        Notification limits on iOS and Android
        Battery drain from background sync
        Widget and watch platform constraints
        Offline logging and sync conflicts
      UX
        Too many features for a simple habit
        Guilt-inducing design
        Hard to use for older adults
        Time zones and travel reset the day
```

---

## How the branches connect

| User need | Features that serve it | Problem to watch |
|---|---|---|
| Know how much to drink | Personalized goal, weather and workout adjustments | Wrong goals for people on fluid restriction; overhydration |
| Remember to drink | Adaptive reminders, calendar-aware pause, quiet hours | Reminder fatigue, so users turn notifications off |
| Log with almost no effort | Quick-add presets, widgets, watch, voice, smart bottle | Guessed volumes and double counting reduce accuracy |
| See progress and stay motivated | Daily ring, streaks, trends, badges | Novelty wears off; a broken streak can cause churn |
| Health-driven needs | Health profiles, clinician-set goals, export | Implying medical advice; regulatory exposure |
| Fit into existing life | Health app sync, beverage types, privacy controls | Sensitive health data; sync conflicts |

## Key assumptions to test first

1. **Logging friction is the main reason people stop.** Test: compare 7-day retention for widget-first logging against in-app-only logging.
2. **Adaptive reminders beat fixed-interval reminders.** Test: A/B test the notification opt-out rate and the number of days users hit their goal.
3. **Streaks help more than they hurt.** Test: compare churn after a broken streak with and without a "streak freeze."
4. **Users will pay for insights or smart-bottle sync.** Test: put a fake-door premium screen in front of users and measure the tap-through rate.

## Suggested MVP cut

- **In:** onboarding with a personalized goal, one-tap logging, a home-screen widget, adaptive reminders, the daily ring and a 7-day trend, Apple Health and Health Connect sync, and a basic streak.
- **Later:** beverage hydration factors, weather and workout adjustments, a watch app, badges, and challenges.
- **Not now:** smart-bottle hardware, social features, clinician mode. These need validated demand and a safety and regulatory review first.
