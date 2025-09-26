# Submission Notes

## Time Allocation Summary
- **60 mins**: Understanding context and reviewing the existing codebase, analyzing the problem statement and user requirements
- **~60 mins**: Implementing the alternative rent tracking solution, moving from manual flags to automatic detection based on lease payment data

## Assumptions Made

### Business Logic Assumptions
- **Rent due dates are lease-specific**: Each lease can have its own payment due date rather than a global monthly cycle
- **Payment tracking is sufficient**: Recording the last payment date is adequate for determining late status (vs. tracking all payment history)
- **Active leases only**: Only currently active leases (not expired) should be considered for late rent detection
- **Single payment per period**: Tenants make one payment per due date cycle rather than partial payments

### Technical Assumptions
- **No payment amount tracking**: Focus on payment dates rather than partial payment amounts or outstanding balances
- **No notification system**: Late rent detection doesn't trigger automated notifications (future enhancement)

## Next Steps (If More Time Available)

### Immediate Enhancements
2. **Validation improvements**: Add business rule validation (e.g., payment date cannot be in the future, due date validation)
3. **Error handling**: Enhance error messages and add proper exception handling for edge cases

### Advanced Features
1. **Payment history tracking**: Implement full payment record system with amounts, partial payments, and payment methods
2. **Automated notifications**: Add email/SMS alerts for upcoming and overdue rent payments
4. **Grace period configuration**: Allow property managers to set grace periods before marking rent as late

### Testing & Quality
1. **Comprehensive testing**: Unit tests for business logic, integration tests for GraphQL resolvers
3. **Documentation**: API documentation and property manager user guides