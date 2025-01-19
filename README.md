# Log Processor Implementation Guide

![Screenshot 2025-01-20 at 3 34 50 AM](https://github.com/user-attachments/assets/6ee8c377-5bc1-4966-ac96-4c1d26aa734a)

## Part 1: Implementation Details

### Function Design
- **Input**: A string containing log entries
- **Output**: A dictionary containing:
  - `total_errors`: Count of all error occurrences
  - `unique_error_messages`: List of unique error messages

### Core Logic
The implementation will utilize regular expressions to parse log entries and extract error messages with the following approach:

1. Parse log entries to identify ERROR level messages
2. Count total ERROR occurrences
3. Collect and alphabetically sort unique error messages
4. Handle edge cases and malformed inputs

### Implementation Steps

#### 1. Function Development
The main function `process_log_file` will be implemented with these considerations:

- Regular expression pattern matching for ERROR entries
- Message extraction and counting logic
- Comprehensive error handling for:
  - Empty input validation
  - Malformed input detection
  - Input type verification
- Type hints for improved code clarity

#### 2. Testing Strategy
Develop unit tests to verify:
- Basic functionality with valid inputs
- Edge case handling
- Error handling for invalid inputs
- Sorting and uniqueness requirements

## Part 2: AWS Deployment & Demo

![Screenshot 2025-01-20 at 3 34 57 AM](https://github.com/user-attachments/assets/3392657e-737c-4211-af0e-e515864d94bf)


### AWS Lambda Configuration
- **Runtime**: Python 3.9+
- **Memory Allocation**: 128 MB
- **Timeout Setting**: 30 seconds
- **IAM Role**: Basic Lambda execution role
  - Includes CloudWatch logging permissions

### Lambda Function Structure
```python
def lambda_handler(event, context):
    # Implementation details here
    pass
```

### API Gateway Integration (Optional)
- REST API endpoint creation
- Testing procedures:
  - Postman verification
  - cURL command testing    
![Screenshot 2025-01-20 at 4 39 10 AM](https://github.com/user-attachments/assets/fbba131d-3c67-4cb9-869b-cb863d41c65c)
