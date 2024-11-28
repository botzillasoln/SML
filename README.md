perform_extrapolation <- function(x, y, new_x) {
model <- lm(y ~ x)
  predicted_y <- predict(model, newdata = data.frame(x = new_x))
   cat("Linear model coefficients:\n")
  print(coef(model))
    cat("\nExtrapolated values for new_x:", new_x, "\n")
  print(predicted_y)
}
