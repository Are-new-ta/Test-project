# Test-projec

const Card = ({ card }) => {
  return (
    <div className='cards__card card'>
      <div className='card__wrapper'>
        <LikeButton parentClass='card' card={card} />
        <PreviewImage card={card} parentClass='card' />
        <p className='card__title'>
          {card?.name || 'Название бота, которое может занимать 2 строки'}
        </p>
        <Rating ratingCard={card?.rating} />
        <p className='card__about'>
          {card?.description ||
            'Описание бота, которое может занимать 3 строки. Описание бота, которое может занимать 3 строки.'}
        </p>
      </div>
      <div className='card__wrapper'>
        <p className='card__price'>{convertToLocaleStringRub(card?.price)}</p>
        <CartButton parentClass='card' card={card} />
      </div>
    </div>
  );
};

export default Card;