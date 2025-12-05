# Feedback Survey

A survey form to collect customer feedback.

```xml
<body>
    <form>
        <section header="Experience">
            <text>How would you rate your experience?</text>
            <slider key="rating" value="5" range="from:1;to:10;step:1;type:int">Rating (1-10)</slider>
        </section>
        <section header="Details">
            <texteditor key="comments" value="">Please share your thoughts...</texteditor>
        </section>
        <section header="Contact">
            <toggle key="anonymous" value="true">Submit Anonymously</toggle>
            <textfield key="contactEmail">Email (Optional)</textfield>
        </section>
    </form>
</body>
```
<img src="/Screenshots/Examples/Advanced/FeedbackSurvey_1.png" width="250" alt="Screenshot">
