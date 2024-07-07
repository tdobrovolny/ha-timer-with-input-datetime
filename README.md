# Home Assistant Timer with Input Datetime Blueprint

This Home Assistant blueprint enables the creation of a timer that can be set and adjusted through the Home Assistant user interface using an `input_datetime` entity. This method provides a flexible way to manage time-based automations directly from the dashboard.

## Features

- **User-Friendly Interface**: Easily set timers using a time input in the UI.
- **Precision Timing**: Specify exact hours and minutes for your timers.
- **Reusable**: Use this blueprint to add timer functionality to any automation requiring precise time control.

## Prerequisites

Before using this blueprint, you should have:

- Home Assistant installed.
- Basic understanding of Home Assistant configuration and automation.

## Installation

1. **Add the Blueprint**:
   - Navigate to the Home Assistant UI, go to Configuration > Blueprints.
   - Click on the import blueprint button and use this URL to import: `https://github.com/tdobrovolny/ha-timer-with-input-datetime/blueprints/automation/timer_with_input_datetime.yaml`

2. **Create the Required Entities**:
   Add the following to your `configuration.yaml` file:

   ```yaml
   input_datetime:
     timer_duration:
       name: Timer Duration
       has_date: false
       has_time: true

   timer:
     my_timer:
       duration: '00:00:00'
    ```

## Using the Blueprint

1. **Create a New Automation from the Blueprint**:

        - Go to Configuration > Automations.
        - Click the “+ ADD AUTOMATION” button.
        - Select “Use Blueprint”.
        - Choose “Timer with Input Datetime” from the list.

    2. **Configure the Automation:**
        For *Input Datetime Entity*, select the input_datetime entity you created (e.g., `input_datetime.timer_duration`).
        For *Timer Entity*, select the timer entity you created (e.g., `timer.my_timer`).

    3. Save and Test:
       - Save the automation.
       - Set the desired timer duration using the input datetime helper on your dashboard.
       - The timer should start with the set duration.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contributions

Contributions are welcome! Please open an issue or submit a pull request with your enhancements or bug fixes.

## Support

If you encounter any issues or have questions, please open an issue in this repository.
